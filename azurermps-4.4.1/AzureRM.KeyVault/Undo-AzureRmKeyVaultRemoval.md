---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
ms.openlocfilehash: 57fdddfea449bbde18762afaed0c576c2b4d1db3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625167"
---
# <span data-ttu-id="89274-101">Undo-AzureRmKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="89274-101">Undo-AzureRmKeyVaultRemoval</span></span>

## <span data-ttu-id="89274-102">摘要</span><span class="sxs-lookup"><span data-stu-id="89274-102">SYNOPSIS</span></span>
<span data-ttu-id="89274-103">將已刪除的金鑰電子倉庫恢復成作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="89274-103">Recovers a deleted key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89274-104">句法</span><span class="sxs-lookup"><span data-stu-id="89274-104">SYNTAX</span></span>

```
Undo-AzureRmKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89274-105">說明</span><span class="sxs-lookup"><span data-stu-id="89274-105">DESCRIPTION</span></span>
<span data-ttu-id="89274-106">**Undo AzureRmKeyVaultRemoval** Cmdlet 會復原先前刪除的主要保存庫。</span><span class="sxs-lookup"><span data-stu-id="89274-106">The **Undo-AzureRmKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="89274-107">復原後的電子倉庫將在恢復後生效</span><span class="sxs-lookup"><span data-stu-id="89274-107">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="89274-108">示例</span><span class="sxs-lookup"><span data-stu-id="89274-108">EXAMPLES</span></span>

### <span data-ttu-id="89274-109">範例1</span><span class="sxs-lookup"><span data-stu-id="89274-109">Example 1</span></span>
```
PS C:\> Undo-AzureRmKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}
```

<span data-ttu-id="89274-110">這個命令會將先前從 eastus2 區域和 "MyResourceGroup" 資源群組中刪除的主要保存庫 ' MyKeyVault ' 復原為作用中且可用的狀態。</span><span class="sxs-lookup"><span data-stu-id="89274-110">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="89274-111">它也會將標記取代為 [新增標籤]。</span><span class="sxs-lookup"><span data-stu-id="89274-111">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="89274-112">參數</span><span class="sxs-lookup"><span data-stu-id="89274-112">PARAMETERS</span></span>

### <span data-ttu-id="89274-113">-位置</span><span class="sxs-lookup"><span data-stu-id="89274-113">-Location</span></span>
<span data-ttu-id="89274-114">指定已刪除的保存庫原始 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="89274-114">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89274-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89274-115">-ResourceGroupName</span></span>
<span data-ttu-id="89274-116">指定要在其中建立金鑰保存庫的現有資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="89274-116">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89274-117">-Tag</span><span class="sxs-lookup"><span data-stu-id="89274-117">-Tag</span></span>
<span data-ttu-id="89274-118">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="89274-118">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="89274-119">例如：</span><span class="sxs-lookup"><span data-stu-id="89274-119">For example:</span></span>

<span data-ttu-id="89274-120">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="89274-120">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89274-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="89274-121">-VaultName</span></span>
<span data-ttu-id="89274-122">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="89274-122">Vault name.</span></span>
<span data-ttu-id="89274-123">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="89274-123">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89274-124">-確認</span><span class="sxs-lookup"><span data-stu-id="89274-124">-Confirm</span></span>
<span data-ttu-id="89274-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="89274-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89274-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89274-126">-WhatIf</span></span>
<span data-ttu-id="89274-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="89274-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89274-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="89274-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89274-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89274-129">-DefaultProfile</span></span>
<span data-ttu-id="89274-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="89274-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89274-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89274-131">CommonParameters</span></span>
<span data-ttu-id="89274-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="89274-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89274-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="89274-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89274-134">輸入</span><span class="sxs-lookup"><span data-stu-id="89274-134">INPUTS</span></span>

### <span data-ttu-id="89274-135">System.object</span><span class="sxs-lookup"><span data-stu-id="89274-135">System.String</span></span>
<span data-ttu-id="89274-136">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="89274-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="89274-137">輸出</span><span class="sxs-lookup"><span data-stu-id="89274-137">OUTPUTS</span></span>

### <span data-ttu-id="89274-138">PSVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="89274-138">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="89274-139">筆記</span><span class="sxs-lookup"><span data-stu-id="89274-139">NOTES</span></span>

## <span data-ttu-id="89274-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="89274-140">RELATED LINKS</span></span>

[<span data-ttu-id="89274-141">移除-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="89274-141">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)

[<span data-ttu-id="89274-142">新-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="89274-142">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="89274-143">AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="89274-143">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)
