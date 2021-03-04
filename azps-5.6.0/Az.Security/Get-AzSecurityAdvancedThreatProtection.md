---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: ec35304bf6c376747fa6f98e7fb5753293e579b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916495"
---
# <span data-ttu-id="ebf3f-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="ebf3f-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="ebf3f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ebf3f-102">SYNOPSIS</span></span>
<span data-ttu-id="ebf3f-103">針對儲存/管理DB 帳戶，獲得進位威脅防護政策。</span><span class="sxs-lookup"><span data-stu-id="ebf3f-103">Gets the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="ebf3f-104">語法</span><span class="sxs-lookup"><span data-stu-id="ebf3f-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ebf3f-105">描述</span><span class="sxs-lookup"><span data-stu-id="ebf3f-105">DESCRIPTION</span></span>
<span data-ttu-id="ebf3f-106">`Get-AzSecurityAdvancedThreatProtection`Cmdlet 會針對儲存/管理DB 帳戶獲得威脅防護政策。</span><span class="sxs-lookup"><span data-stu-id="ebf3f-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="ebf3f-107">若要使用此 Cmdlet，請指定 *ResourceId* 參數。</span><span class="sxs-lookup"><span data-stu-id="ebf3f-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="ebf3f-108">例子</span><span class="sxs-lookup"><span data-stu-id="ebf3f-108">EXAMPLES</span></span>

### <span data-ttu-id="ebf3f-109">範例 1：儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="ebf3f-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="ebf3f-110">此命令會針對資源識別碼獲得進位威脅防護策略 `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` 。</span><span class="sxs-lookup"><span data-stu-id="ebf3f-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="ebf3f-111">範例 2：管理資料庫帳戶</span><span class="sxs-lookup"><span data-stu-id="ebf3f-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="ebf3f-112">此命令會針對資源識別碼獲得進位威脅防護策略 ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` 。</span><span class="sxs-lookup"><span data-stu-id="ebf3f-112">This command gets the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="ebf3f-113">參數</span><span class="sxs-lookup"><span data-stu-id="ebf3f-113">PARAMETERS</span></span>

### <span data-ttu-id="ebf3f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebf3f-114">-DefaultProfile</span></span>
<span data-ttu-id="ebf3f-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ebf3f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebf3f-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ebf3f-116">-ResourceId</span></span>
<span data-ttu-id="ebf3f-117">這是要調用命令之安全性資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ebf3f-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="ebf3f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebf3f-118">CommonParameters</span></span>
<span data-ttu-id="ebf3f-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ebf3f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebf3f-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ebf3f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebf3f-121">輸入</span><span class="sxs-lookup"><span data-stu-id="ebf3f-121">INPUTS</span></span>

### <span data-ttu-id="ebf3f-122">System.String</span><span class="sxs-lookup"><span data-stu-id="ebf3f-122">System.String</span></span>

## <span data-ttu-id="ebf3f-123">輸出</span><span class="sxs-lookup"><span data-stu-id="ebf3f-123">OUTPUTS</span></span>

### <span data-ttu-id="ebf3f-124">Microsoft.Azure.Commands.Security.models.AdvancedThreatProtection.PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="ebf3f-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="ebf3f-125">筆記</span><span class="sxs-lookup"><span data-stu-id="ebf3f-125">NOTES</span></span>

## <span data-ttu-id="ebf3f-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="ebf3f-126">RELATED LINKS</span></span>
