---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: e4412d770f47bda0de735b315d638c0b8fdb26df
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280041"
---
# <span data-ttu-id="2c49c-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="2c49c-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="2c49c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2c49c-102">SYNOPSIS</span></span>
<span data-ttu-id="2c49c-103">取得儲存/cosmosDB 帳戶的高級威脅防護原則。</span><span class="sxs-lookup"><span data-stu-id="2c49c-103">Gets the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="2c49c-104">句法</span><span class="sxs-lookup"><span data-stu-id="2c49c-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2c49c-105">說明</span><span class="sxs-lookup"><span data-stu-id="2c49c-105">DESCRIPTION</span></span>
<span data-ttu-id="2c49c-106">這個 `Get-AzSecurityAdvancedThreatProtection` Cmdlet 會取得儲存/cosmosDB 帳戶的威脅防護原則。</span><span class="sxs-lookup"><span data-stu-id="2c49c-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="2c49c-107">若要使用這個 Cmdlet，請指定 *ResourceId* 參數。</span><span class="sxs-lookup"><span data-stu-id="2c49c-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="2c49c-108">示例</span><span class="sxs-lookup"><span data-stu-id="2c49c-108">EXAMPLES</span></span>

### <span data-ttu-id="2c49c-109">範例1：儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="2c49c-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="2c49c-110">這個命令會取得資源識別碼的高級威脅防護原則 `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` 。</span><span class="sxs-lookup"><span data-stu-id="2c49c-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="2c49c-111">範例2： CosmosDB 帳戶</span><span class="sxs-lookup"><span data-stu-id="2c49c-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="2c49c-112">這個命令會取得資源識別碼的高級威脅防護原則 ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` 。</span><span class="sxs-lookup"><span data-stu-id="2c49c-112">This command gets the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="2c49c-113">參數</span><span class="sxs-lookup"><span data-stu-id="2c49c-113">PARAMETERS</span></span>

### <span data-ttu-id="2c49c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c49c-114">-DefaultProfile</span></span>
<span data-ttu-id="2c49c-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2c49c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c49c-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c49c-116">-ResourceId</span></span>
<span data-ttu-id="2c49c-117">您想要在其上喚醒命令的安全性資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2c49c-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="2c49c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c49c-118">CommonParameters</span></span>
<span data-ttu-id="2c49c-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2c49c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c49c-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2c49c-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c49c-121">輸入</span><span class="sxs-lookup"><span data-stu-id="2c49c-121">INPUTS</span></span>

### <span data-ttu-id="2c49c-122">System.object</span><span class="sxs-lookup"><span data-stu-id="2c49c-122">System.String</span></span>

## <span data-ttu-id="2c49c-123">輸出</span><span class="sxs-lookup"><span data-stu-id="2c49c-123">OUTPUTS</span></span>

### <span data-ttu-id="2c49c-124">PSAdvancedThreatProtection 中的 AdvancedThreatProtection （Security..。</span><span class="sxs-lookup"><span data-stu-id="2c49c-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="2c49c-125">筆記</span><span class="sxs-lookup"><span data-stu-id="2c49c-125">NOTES</span></span>

## <span data-ttu-id="2c49c-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c49c-126">RELATED LINKS</span></span>
