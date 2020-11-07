---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
ms.openlocfilehash: fd2483925e8ab14772a3bf34d4411748583a03c9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794645"
---
# <span data-ttu-id="eaf5a-101">Undo-AzKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="eaf5a-101">Undo-AzKeyVaultRemoval</span></span>

## <span data-ttu-id="eaf5a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eaf5a-102">SYNOPSIS</span></span>
<span data-ttu-id="eaf5a-103">將已刪除的金鑰電子倉庫恢復成作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="eaf5a-103">Recovers a deleted key vault into an active state.</span></span>

## <span data-ttu-id="eaf5a-104">句法</span><span class="sxs-lookup"><span data-stu-id="eaf5a-104">SYNTAX</span></span>

```
Undo-AzKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eaf5a-105">說明</span><span class="sxs-lookup"><span data-stu-id="eaf5a-105">DESCRIPTION</span></span>
<span data-ttu-id="eaf5a-106">**Undo AzKeyVaultRemoval** Cmdlet 會復原先前刪除的主要保存庫。</span><span class="sxs-lookup"><span data-stu-id="eaf5a-106">The **Undo-AzKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="eaf5a-107">復原後的電子倉庫將在恢復後生效</span><span class="sxs-lookup"><span data-stu-id="eaf5a-107">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="eaf5a-108">示例</span><span class="sxs-lookup"><span data-stu-id="eaf5a-108">EXAMPLES</span></span>

### <span data-ttu-id="eaf5a-109">範例1</span><span class="sxs-lookup"><span data-stu-id="eaf5a-109">Example 1</span></span>
```
PS C:\> Undo-AzKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}
```

<span data-ttu-id="eaf5a-110">這個命令會將先前從 eastus2 區域和 "MyResourceGroup" 資源群組中刪除的主要保存庫 ' MyKeyVault ' 復原為作用中且可用的狀態。</span><span class="sxs-lookup"><span data-stu-id="eaf5a-110">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="eaf5a-111">它也會將標記取代為 [新增標籤]。</span><span class="sxs-lookup"><span data-stu-id="eaf5a-111">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="eaf5a-112">參數</span><span class="sxs-lookup"><span data-stu-id="eaf5a-112">PARAMETERS</span></span>

### <span data-ttu-id="eaf5a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaf5a-113">-DefaultProfile</span></span>
<span data-ttu-id="eaf5a-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="eaf5a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf5a-115">-位置</span><span class="sxs-lookup"><span data-stu-id="eaf5a-115">-Location</span></span>
<span data-ttu-id="eaf5a-116">指定已刪除的保存庫原始 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="eaf5a-116">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaf5a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaf5a-117">-ResourceGroupName</span></span>
<span data-ttu-id="eaf5a-118">指定要在其中建立金鑰保存庫的現有資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="eaf5a-118">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaf5a-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="eaf5a-119">-Tag</span></span>
<span data-ttu-id="eaf5a-120">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="eaf5a-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="eaf5a-121">例如：</span><span class="sxs-lookup"><span data-stu-id="eaf5a-121">For example:</span></span>

<span data-ttu-id="eaf5a-122">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="eaf5a-122">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaf5a-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="eaf5a-123">-VaultName</span></span>
<span data-ttu-id="eaf5a-124">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="eaf5a-124">Vault name.</span></span>
<span data-ttu-id="eaf5a-125">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="eaf5a-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaf5a-126">-確認</span><span class="sxs-lookup"><span data-stu-id="eaf5a-126">-Confirm</span></span>
<span data-ttu-id="eaf5a-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="eaf5a-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf5a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaf5a-128">-WhatIf</span></span>
<span data-ttu-id="eaf5a-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eaf5a-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eaf5a-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eaf5a-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf5a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaf5a-131">CommonParameters</span></span>
<span data-ttu-id="eaf5a-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eaf5a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaf5a-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eaf5a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaf5a-134">輸入</span><span class="sxs-lookup"><span data-stu-id="eaf5a-134">INPUTS</span></span>

### <span data-ttu-id="eaf5a-135">System.object</span><span class="sxs-lookup"><span data-stu-id="eaf5a-135">System.String</span></span>
<span data-ttu-id="eaf5a-136">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="eaf5a-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="eaf5a-137">輸出</span><span class="sxs-lookup"><span data-stu-id="eaf5a-137">OUTPUTS</span></span>

### <span data-ttu-id="eaf5a-138">PSVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="eaf5a-138">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="eaf5a-139">筆記</span><span class="sxs-lookup"><span data-stu-id="eaf5a-139">NOTES</span></span>

## <span data-ttu-id="eaf5a-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="eaf5a-140">RELATED LINKS</span></span>

[<span data-ttu-id="eaf5a-141">移除-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="eaf5a-141">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)

[<span data-ttu-id="eaf5a-142">新-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="eaf5a-142">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="eaf5a-143">AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="eaf5a-143">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)
