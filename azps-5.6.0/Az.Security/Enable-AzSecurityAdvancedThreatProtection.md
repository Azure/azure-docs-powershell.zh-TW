---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/enable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 10bda682881f35bc8401bec7304dcc1a68fd1d66
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910650"
---
# <span data-ttu-id="7187e-101">Enable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="7187e-101">Enable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="7187e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7187e-102">SYNOPSIS</span></span>
<span data-ttu-id="7187e-103">針對儲存/管理DB 帳戶啟用進位威脅防護政策。</span><span class="sxs-lookup"><span data-stu-id="7187e-103">Enables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="7187e-104">語法</span><span class="sxs-lookup"><span data-stu-id="7187e-104">SYNTAX</span></span>

```
Enable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7187e-105">描述</span><span class="sxs-lookup"><span data-stu-id="7187e-105">DESCRIPTION</span></span>
<span data-ttu-id="7187e-106">`Enable-AzSecurityAdvancedThreatProtection`Cmdlet 會針對儲存/管理DB 帳戶啟用威脅防護策略。</span><span class="sxs-lookup"><span data-stu-id="7187e-106">The `Enable-AzSecurityAdvancedThreatProtection` cmdlet enables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="7187e-107">若要使用此 Cmdlet，請指定 *ResourceId* 參數。</span><span class="sxs-lookup"><span data-stu-id="7187e-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="7187e-108">例子</span><span class="sxs-lookup"><span data-stu-id="7187e-108">EXAMPLES</span></span>

### <span data-ttu-id="7187e-109">範例 1：儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="7187e-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="7187e-110">此命令會針對資源識別碼啟用進位威脅防護策略 `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` 。</span><span class="sxs-lookup"><span data-stu-id="7187e-110">This command enables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="7187e-111">範例 2：管理資料庫帳戶</span><span class="sxs-lookup"><span data-stu-id="7187e-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="7187e-112">此命令會針對資源識別碼啟用進位威脅防護策略 ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` 。</span><span class="sxs-lookup"><span data-stu-id="7187e-112">This command enables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="7187e-113">參數</span><span class="sxs-lookup"><span data-stu-id="7187e-113">PARAMETERS</span></span>

### <span data-ttu-id="7187e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7187e-114">-DefaultProfile</span></span>
<span data-ttu-id="7187e-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7187e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7187e-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7187e-116">-ResourceId</span></span>
<span data-ttu-id="7187e-117">這是要調用命令之安全性資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7187e-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="7187e-118">-確認</span><span class="sxs-lookup"><span data-stu-id="7187e-118">-Confirm</span></span>
<span data-ttu-id="7187e-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7187e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7187e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7187e-120">-WhatIf</span></span>
<span data-ttu-id="7187e-121">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7187e-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7187e-122">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7187e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7187e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7187e-123">CommonParameters</span></span>
<span data-ttu-id="7187e-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7187e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7187e-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7187e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7187e-126">輸入</span><span class="sxs-lookup"><span data-stu-id="7187e-126">INPUTS</span></span>

### <span data-ttu-id="7187e-127">沒有</span><span class="sxs-lookup"><span data-stu-id="7187e-127">None</span></span>

## <span data-ttu-id="7187e-128">輸出</span><span class="sxs-lookup"><span data-stu-id="7187e-128">OUTPUTS</span></span>

### <span data-ttu-id="7187e-129">Microsoft.Azure.Commands.Security.models.AdvancedThreatProtection.PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="7187e-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="7187e-130">筆記</span><span class="sxs-lookup"><span data-stu-id="7187e-130">NOTES</span></span>

## <span data-ttu-id="7187e-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="7187e-131">RELATED LINKS</span></span>
