---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/new-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 739ce121e26f1010c5c13ff3330dadffa02053af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447085"
---
# <span data-ttu-id="d1091-101">New-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d1091-101">New-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="d1091-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d1091-102">SYNOPSIS</span></span>
<span data-ttu-id="d1091-103">建立 [以位置為基礎的服務帳戶]。</span><span class="sxs-lookup"><span data-stu-id="d1091-103">Creates a Location Based Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1091-104">句法</span><span class="sxs-lookup"><span data-stu-id="d1091-104">SYNTAX</span></span>

```
New-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d1091-105">說明</span><span class="sxs-lookup"><span data-stu-id="d1091-105">DESCRIPTION</span></span>
<span data-ttu-id="d1091-106">**AzureRmLocationBasedServicesAccount** Cmdlet 會使用指定的 SKU 建立一個以位置為基礎的服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="d1091-106">The **New-AzureRmLocationBasedServicesAccount** cmdlet creates a Location Based Services account with the specified SKU.</span></span>

## <span data-ttu-id="d1091-107">示例</span><span class="sxs-lookup"><span data-stu-id="d1091-107">EXAMPLES</span></span>

### <span data-ttu-id="d1091-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d1091-108">Example 1</span></span>
```
PS C:\> New-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

Notice
By creating a Location Based Account, you are consenting to the terms of use (see https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/).
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): y

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="d1091-109">使用 SKU S0 和標記在 [資源群組 MyResourceGroup] 中建立名為「我的帳戶」的新位置的服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="d1091-109">Creates a new Location Based Services account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="d1091-110">參數</span><span class="sxs-lookup"><span data-stu-id="d1091-110">PARAMETERS</span></span>

### <span data-ttu-id="d1091-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1091-111">-DefaultProfile</span></span>
<span data-ttu-id="d1091-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d1091-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1091-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d1091-113">-Force</span></span>
<span data-ttu-id="d1091-114">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="d1091-114">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1091-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="d1091-115">-Name</span></span>
<span data-ttu-id="d1091-116">[以位置為基礎的服務] 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d1091-116">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1091-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1091-117">-ResourceGroupName</span></span>
<span data-ttu-id="d1091-118">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d1091-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="d1091-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d1091-119">-SkuName</span></span>
<span data-ttu-id="d1091-120">[以位置為基礎的服務帳戶] Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="d1091-120">Location Based Services Account Sku Name.</span></span>

<span data-ttu-id="d1091-121">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d1091-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d1091-122">S0</span><span class="sxs-lookup"><span data-stu-id="d1091-122">S0</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: S0

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1091-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="d1091-123">-Tag</span></span>
<span data-ttu-id="d1091-124">[以位置為基礎的服務] 帳戶標記。</span><span class="sxs-lookup"><span data-stu-id="d1091-124">Location Based Services Account Tags.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1091-125">-確認</span><span class="sxs-lookup"><span data-stu-id="d1091-125">-Confirm</span></span>
<span data-ttu-id="d1091-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d1091-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1091-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1091-127">-WhatIf</span></span>
<span data-ttu-id="d1091-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d1091-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1091-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d1091-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1091-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1091-130">CommonParameters</span></span>
<span data-ttu-id="d1091-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d1091-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1091-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d1091-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1091-133">輸入</span><span class="sxs-lookup"><span data-stu-id="d1091-133">INPUTS</span></span>

### <span data-ttu-id="d1091-134">System.object</span><span class="sxs-lookup"><span data-stu-id="d1091-134">System.String</span></span>

## <span data-ttu-id="d1091-135">輸出</span><span class="sxs-lookup"><span data-stu-id="d1091-135">OUTPUTS</span></span>

### <span data-ttu-id="d1091-136">PSLocationBasedServicesAccount 中的 LocationBasedServices。</span><span class="sxs-lookup"><span data-stu-id="d1091-136">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccount</span></span>

## <span data-ttu-id="d1091-137">筆記</span><span class="sxs-lookup"><span data-stu-id="d1091-137">NOTES</span></span>

<span data-ttu-id="d1091-138">建立 [以位置為基礎的服務] 帳戶必須在 (請參閱，然後接聽接收詞彙的提示 https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/) 。</span><span class="sxs-lookup"><span data-stu-id="d1091-138">Creating a Location Based Services account requires answering a prompt to accept terms (see https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/).</span></span>  <span data-ttu-id="d1091-139">-Force 參數可用來表示接受字詞。</span><span class="sxs-lookup"><span data-stu-id="d1091-139">The -Force parameter can be used to indicate acceptance of the terms.</span></span>

## <span data-ttu-id="d1091-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="d1091-140">RELATED LINKS</span></span>
