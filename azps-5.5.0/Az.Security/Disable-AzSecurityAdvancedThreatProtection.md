---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/disable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: e7195131830fd5b19a6d67b4fae5583374da7d0f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128342"
---
# <span data-ttu-id="95176-101">Disable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="95176-101">Disable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="95176-102">摘要</span><span class="sxs-lookup"><span data-stu-id="95176-102">SYNOPSIS</span></span>
<span data-ttu-id="95176-103">針對 [儲存/cosmosDB] 帳戶停用 [高級威脅防護原則]。</span><span class="sxs-lookup"><span data-stu-id="95176-103">Disables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="95176-104">句法</span><span class="sxs-lookup"><span data-stu-id="95176-104">SYNTAX</span></span>

```
Disable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95176-105">說明</span><span class="sxs-lookup"><span data-stu-id="95176-105">DESCRIPTION</span></span>
<span data-ttu-id="95176-106">此 `Disable-AzSecurityAdvancedThreatProtection` Cmdlet 會針對儲存/cosmosDB 帳戶停用威脅防護原則。</span><span class="sxs-lookup"><span data-stu-id="95176-106">The `Disable-AzSecurityAdvancedThreatProtection` cmdlet disables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="95176-107">若要使用這個 Cmdlet，請指定 *ResourceId* 參數。</span><span class="sxs-lookup"><span data-stu-id="95176-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="95176-108">示例</span><span class="sxs-lookup"><span data-stu-id="95176-108">EXAMPLES</span></span>

### <span data-ttu-id="95176-109">範例1：儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="95176-109">Example 1 : Storage Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="95176-110">這個命令會停用 [資源識別碼] 的高級威脅防護原則 `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` 。</span><span class="sxs-lookup"><span data-stu-id="95176-110">This command disables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="95176-111">範例2： CosmosDB 帳戶</span><span class="sxs-lookup"><span data-stu-id="95176-111">Example 2 : CosmosDB Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="95176-112">這個命令會停用 [資源識別碼] 的高級威脅防護原則 ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` 。</span><span class="sxs-lookup"><span data-stu-id="95176-112">This command disables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="95176-113">參數</span><span class="sxs-lookup"><span data-stu-id="95176-113">PARAMETERS</span></span>

### <span data-ttu-id="95176-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95176-114">-DefaultProfile</span></span>
<span data-ttu-id="95176-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="95176-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95176-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95176-116">-ResourceId</span></span>
<span data-ttu-id="95176-117">您想要在其上喚醒命令的安全性資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="95176-117">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95176-118">-確認</span><span class="sxs-lookup"><span data-stu-id="95176-118">-Confirm</span></span>
<span data-ttu-id="95176-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="95176-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95176-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95176-120">-WhatIf</span></span>
<span data-ttu-id="95176-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="95176-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95176-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95176-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95176-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95176-123">CommonParameters</span></span>
<span data-ttu-id="95176-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="95176-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95176-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="95176-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95176-126">輸入</span><span class="sxs-lookup"><span data-stu-id="95176-126">INPUTS</span></span>

### <span data-ttu-id="95176-127">所有</span><span class="sxs-lookup"><span data-stu-id="95176-127">None</span></span>

## <span data-ttu-id="95176-128">輸出</span><span class="sxs-lookup"><span data-stu-id="95176-128">OUTPUTS</span></span>

### <span data-ttu-id="95176-129">PSAdvancedThreatProtection 中的 AdvancedThreatProtection （Security..。</span><span class="sxs-lookup"><span data-stu-id="95176-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="95176-130">筆記</span><span class="sxs-lookup"><span data-stu-id="95176-130">NOTES</span></span>

## <span data-ttu-id="95176-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="95176-131">RELATED LINKS</span></span>
