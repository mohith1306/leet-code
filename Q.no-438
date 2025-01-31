class Solution {
    public List<Integer> findAnagrams(String s, String p) {
        HashMap<Character, Integer> map1 = new HashMap<>();
        for (char ch : p.toCharArray()) {
            map1.put(ch, map1.getOrDefault(ch, 0) + 1);
        }
        int len1 = p.length();
        int len2 = s.length();
        List<Integer> list = new ArrayList<>();
        if (len1 > len2) return list;
        HashMap<Character, Integer> map2 = new HashMap<>();
        for (int i = 0; i < len1; i++) {
            map2.put(s.charAt(i), map2.getOrDefault(s.charAt(i), 0) + 1);
        }
        if (map1.equals(map2)) {
            list.add(0);
        }
        int i = 1;
        int j = len1;
        while (j < len2) {
            char leftChar = s.charAt(i - 1);
            map2.put(leftChar, map2.get(leftChar) - 1);
            if (map2.get(leftChar) == 0) {
                map2.remove(leftChar);
            }
            char rightChar = s.charAt(j);
            map2.put(rightChar, map2.getOrDefault(rightChar, 0) + 1);

            if (map1.equals(map2)) {
                list.add(i);
            }

            i++;
            j++;
        }

        return list;
    }
}
