---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurermkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
ms.openlocfilehash: 83737a7643c78ef4ec41d84e153690b3a53a8d5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625895"
---
# <span data-ttu-id="0a8b6-101">Undo-AzureRmKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="0a8b6-101">Undo-AzureRmKeyVaultRemoval</span></span>

## <span data-ttu-id="0a8b6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0a8b6-102">SYNOPSIS</span></span>
<span data-ttu-id="0a8b6-103">將已刪除的金鑰電子倉庫恢復成作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="0a8b6-103">Recovers a deleted key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a8b6-104">句法</span><span class="sxs-lookup"><span data-stu-id="0a8b6-104">SYNTAX</span></span>

### <span data-ttu-id="0a8b6-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="0a8b6-105">Default (Default)</span></span>
```
Undo-AzureRmKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a8b6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0a8b6-106">InputObject</span></span>
```
Undo-AzureRmKeyVaultRemoval [-InputObject] <PSDeletedKeyVault> [-ResourceGroupName] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a8b6-107">說明</span><span class="sxs-lookup"><span data-stu-id="0a8b6-107">DESCRIPTION</span></span>
<span data-ttu-id="0a8b6-108">**Undo AzureRmKeyVaultRemoval** Cmdlet 會復原先前刪除的主要保存庫。</span><span class="sxs-lookup"><span data-stu-id="0a8b6-108">The **Undo-AzureRmKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="0a8b6-109">復原後的電子倉庫將在恢復後生效</span><span class="sxs-lookup"><span data-stu-id="0a8b6-109">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="0a8b6-110">示例</span><span class="sxs-lookup"><span data-stu-id="0a8b6-110">EXAMPLES</span></span>

### <span data-ttu-id="0a8b6-111">範例1</span><span class="sxs-lookup"><span data-stu-id="0a8b6-111">Example 1</span></span>
```
PS C:\> Undo-AzureRmKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}
```

<span data-ttu-id="0a8b6-112">這個命令會將先前從 eastus2 區域和 "MyResourceGroup" 資源群組中刪除的主要保存庫 ' MyKeyVault ' 復原為作用中且可用的狀態。</span><span class="sxs-lookup"><span data-stu-id="0a8b6-112">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="0a8b6-113">它也會將標記取代為 [新增標籤]。</span><span class="sxs-lookup"><span data-stu-id="0a8b6-113">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="0a8b6-114">參數</span><span class="sxs-lookup"><span data-stu-id="0a8b6-114">PARAMETERS</span></span>

### <span data-ttu-id="0a8b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a8b6-115">-DefaultProfile</span></span>
<span data-ttu-id="0a8b6-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0a8b6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a8b6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a8b6-117">-InputObject</span></span>
<span data-ttu-id="0a8b6-118">已刪除的保存庫物件</span><span class="sxs-lookup"><span data-stu-id="0a8b6-118">Deleted vault object</span></span>

```yaml
Type: PSDeletedKeyVault
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a8b6-119">-位置</span><span class="sxs-lookup"><span data-stu-id="0a8b6-119">-Location</span></span>
<span data-ttu-id="0a8b6-120">指定已刪除的保存庫原始 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="0a8b6-120">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a8b6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a8b6-121">-ResourceGroupName</span></span>
<span data-ttu-id="0a8b6-122">指定要在其中建立金鑰保存庫的現有資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a8b6-122">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="0a8b6-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="0a8b6-123">-Tag</span></span>
<span data-ttu-id="0a8b6-124">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="0a8b6-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0a8b6-125">例如：</span><span class="sxs-lookup"><span data-stu-id="0a8b6-125">For example:</span></span>

<span data-ttu-id="0a8b6-126">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="0a8b6-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0a8b6-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0a8b6-127">-VaultName</span></span>
<span data-ttu-id="0a8b6-128">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="0a8b6-128">Vault name.</span></span>
<span data-ttu-id="0a8b6-129">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="0a8b6-129">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a8b6-130">-確認</span><span class="sxs-lookup"><span data-stu-id="0a8b6-130">-Confirm</span></span>
<span data-ttu-id="0a8b6-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0a8b6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a8b6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a8b6-132">-WhatIf</span></span>
<span data-ttu-id="0a8b6-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0a8b6-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a8b6-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0a8b6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a8b6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a8b6-135">CommonParameters</span></span>
<span data-ttu-id="0a8b6-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0a8b6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a8b6-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0a8b6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a8b6-138">輸入</span><span class="sxs-lookup"><span data-stu-id="0a8b6-138">INPUTS</span></span>

### <span data-ttu-id="0a8b6-139">System.object</span><span class="sxs-lookup"><span data-stu-id="0a8b6-139">System.String</span></span>
<span data-ttu-id="0a8b6-140">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0a8b6-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0a8b6-141">輸出</span><span class="sxs-lookup"><span data-stu-id="0a8b6-141">OUTPUTS</span></span>

### <span data-ttu-id="0a8b6-142">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="0a8b6-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="0a8b6-143">筆記</span><span class="sxs-lookup"><span data-stu-id="0a8b6-143">NOTES</span></span>

## <span data-ttu-id="0a8b6-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a8b6-144">RELATED LINKS</span></span>

[<span data-ttu-id="0a8b6-145">移除-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="0a8b6-145">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)

[<span data-ttu-id="0a8b6-146">新-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="0a8b6-146">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="0a8b6-147">AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="0a8b6-147">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)
