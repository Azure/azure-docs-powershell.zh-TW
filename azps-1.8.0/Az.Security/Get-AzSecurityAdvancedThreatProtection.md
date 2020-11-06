---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 8957a794660750f45f295b77d921e647d368e7dc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620704"
---
# <span data-ttu-id="5ed39-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="5ed39-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="5ed39-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ed39-102">SYNOPSIS</span></span>
<span data-ttu-id="5ed39-103">取得儲存空間帳戶的高級威脅防護原則。</span><span class="sxs-lookup"><span data-stu-id="5ed39-103">Gets the advanced threat protection policy for a storage account.</span></span>

## <span data-ttu-id="5ed39-104">句法</span><span class="sxs-lookup"><span data-stu-id="5ed39-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ed39-105">說明</span><span class="sxs-lookup"><span data-stu-id="5ed39-105">DESCRIPTION</span></span>
<span data-ttu-id="5ed39-106">此 `Get-AzSecurityAdvancedThreatProtection` Cmdlet 會取得儲存空間帳戶的威脅防護原則。</span><span class="sxs-lookup"><span data-stu-id="5ed39-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage account.</span></span>
<span data-ttu-id="5ed39-107">若要使用這個 Cmdlet，請指定 *ResourceId* 參數。</span><span class="sxs-lookup"><span data-stu-id="5ed39-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="5ed39-108">示例</span><span class="sxs-lookup"><span data-stu-id="5ed39-108">EXAMPLES</span></span>

### <span data-ttu-id="5ed39-109">範例1</span><span class="sxs-lookup"><span data-stu-id="5ed39-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="5ed39-110">這個命令會取得資源識別碼的高級威脅防護原則 `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` 。</span><span class="sxs-lookup"><span data-stu-id="5ed39-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

## <span data-ttu-id="5ed39-111">參數</span><span class="sxs-lookup"><span data-stu-id="5ed39-111">PARAMETERS</span></span>

### <span data-ttu-id="5ed39-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ed39-112">-DefaultProfile</span></span>
<span data-ttu-id="5ed39-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5ed39-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ed39-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ed39-114">-ResourceId</span></span>
<span data-ttu-id="5ed39-115">您想要在其上喚醒命令的安全性資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5ed39-115">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="5ed39-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ed39-116">CommonParameters</span></span>
<span data-ttu-id="5ed39-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ed39-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ed39-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5ed39-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ed39-119">輸入</span><span class="sxs-lookup"><span data-stu-id="5ed39-119">INPUTS</span></span>

### <span data-ttu-id="5ed39-120">System.object</span><span class="sxs-lookup"><span data-stu-id="5ed39-120">System.String</span></span>

## <span data-ttu-id="5ed39-121">輸出</span><span class="sxs-lookup"><span data-stu-id="5ed39-121">OUTPUTS</span></span>

### <span data-ttu-id="5ed39-122">PSAdvancedThreatProtection 中的 AdvancedThreatProtection （Security..。</span><span class="sxs-lookup"><span data-stu-id="5ed39-122">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="5ed39-123">筆記</span><span class="sxs-lookup"><span data-stu-id="5ed39-123">NOTES</span></span>

## <span data-ttu-id="5ed39-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ed39-124">RELATED LINKS</span></span>
