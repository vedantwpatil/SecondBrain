$$f(x) = \sum_{k=0}^\infty = \frac{(x-2)^k}{5^k} for -3 < x < 7$$
$$f'(x) = \sum^\infty_{k=0} \frac{d}{dx}\left[ \frac{(x-2)^k}{5^k} \right]$$
$$\sum^\infty_{k=0} \frac{d}{dx} \left[ \frac{1}{5^k}*(x-2)^k \right]$$
$$\sum^\infty_{k =1 } \frac{k}{5^k} (x-2)^{k-1}$$

Find the derivative of the given function 
$$f(x) = \sum^\infty_{k = 0} \frac{(-1)^k}{(2k+1)!}x^{k+1}$$ for all x 

-- Keybindings for LuaSnip
vim.api.nvim_set_keymap("i", "<Tab>", "luasnip#expand_or_jumpable() ? '<Plug>luasnip-expand-or-jump' : '<Tab>'", { expr = true, silent = true })
vim.api.nvim_set_keymap("s", "<Tab>", "luasnip#jumpable(1) ? '<Plug>luasnip-jump-next' : '<Tab>'", { expr = true, silent = true })
