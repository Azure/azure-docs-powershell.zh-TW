---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/get-azurermlocationbasedservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccountKey.md
ms.openlocfilehash: 1f528bb0a80f039b9a2be7cb4cb6e4c7fbc740c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456192"
---
# <span data-ttu-id="defff-101">Get-AzureRmLocationBasedServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="defff-101">Get-AzureRmLocationBasedServicesAccountKey</span></span>

## <span data-ttu-id="defff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="defff-102">SYNOPSIS</span></span>
<span data-ttu-id="defff-103">取得帳戶的 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="defff-103">Gets the API keys for an account.</span></span> <span data-ttu-id="defff-104">這些金鑰是在針對 Azure 位置基礎服務進行後續呼叫時所使用的驗證機制。</span><span class="sxs-lookup"><span data-stu-id="defff-104">These keys are the authentication mechanism used in subsequent calls to Azure Location Based Services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="defff-105">句法</span><span class="sxs-lookup"><span data-stu-id="defff-105">SYNTAX</span></span>

### <span data-ttu-id="defff-106">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="defff-106">NameParameterSet (Default)</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="defff-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="defff-107">InputObjectParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-InputObject <PSLocationBasedServicesAccount>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="defff-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="defff-108">ResourceIdParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="defff-109">說明</span><span class="sxs-lookup"><span data-stu-id="defff-109">DESCRIPTION</span></span>
<span data-ttu-id="defff-110">**AzureRmLocationBasedServicesAccountKey** Cmdlet 會取得預配的位置服務帳戶的 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="defff-110">The **Get-AzureRmLocationBasedServicesAccountKey** cmdlet gets the API keys for a provisioned Location Based Services account.</span></span>

<span data-ttu-id="defff-111">[以位置為基礎的服務] 帳戶有兩個 API 金鑰：主要和次要。</span><span class="sxs-lookup"><span data-stu-id="defff-111">A Location Based Services account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="defff-112">這些金鑰可讓您與 [以位置為基礎的服務] 帳戶端點互動。</span><span class="sxs-lookup"><span data-stu-id="defff-112">The keys enable interaction with the Location Based Services account endpoint.</span></span>

<span data-ttu-id="defff-113">使用 [新-AzureRmLocationBasedServicesAccountKey](New-AzureRmLocationBasedServicesAccountKey.md) 重新產生金鑰。</span><span class="sxs-lookup"><span data-stu-id="defff-113">Use [New-AzureRmLocationBasedServicesAccountKey](New-AzureRmLocationBasedServicesAccountKey.md) to regenerate a key.</span></span>

## <span data-ttu-id="defff-114">示例</span><span class="sxs-lookup"><span data-stu-id="defff-114">EXAMPLES</span></span>

### <span data-ttu-id="defff-115">範例1</span><span class="sxs-lookup"><span data-stu-id="defff-115">Example 1</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="defff-116">傳回 [資源群組 MyResourceGroup] 中名為 [我的帳戶] 的帳戶按鍵。</span><span class="sxs-lookup"><span data-stu-id="defff-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="defff-117">範例2</span><span class="sxs-lookup"><span data-stu-id="defff-117">Example 2</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="defff-118">針對指定的位置服務帳戶傳回金鑰。</span><span class="sxs-lookup"><span data-stu-id="defff-118">Returns the keys for the specified Location Based Services Account.</span></span>

## <span data-ttu-id="defff-119">參數</span><span class="sxs-lookup"><span data-stu-id="defff-119">PARAMETERS</span></span>

### <span data-ttu-id="defff-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="defff-120">-DefaultProfile</span></span>
<span data-ttu-id="defff-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="defff-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="defff-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="defff-122">-InputObject</span></span>
<span data-ttu-id="defff-123">[以位置為基礎的服務] 帳戶從 [AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md)中進行管道。</span><span class="sxs-lookup"><span data-stu-id="defff-123">Location Based Services Account piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span></span>

```yaml
Type: PSLocationBasedServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="defff-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="defff-124">-Name</span></span>
<span data-ttu-id="defff-125">[以位置為基礎的服務] 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="defff-125">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="defff-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="defff-126">-ResourceGroupName</span></span>
<span data-ttu-id="defff-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="defff-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="defff-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="defff-128">-ResourceId</span></span>
<span data-ttu-id="defff-129">基於位置的服務帳戶 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="defff-129">Location Based Services Account ResourceId.</span></span>
```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="defff-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="defff-130">CommonParameters</span></span>
<span data-ttu-id="defff-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="defff-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="defff-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="defff-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="defff-133">輸入</span><span class="sxs-lookup"><span data-stu-id="defff-133">INPUTS</span></span>

### <span data-ttu-id="defff-134">System.object</span><span class="sxs-lookup"><span data-stu-id="defff-134">System.String</span></span>

## <span data-ttu-id="defff-135">輸出</span><span class="sxs-lookup"><span data-stu-id="defff-135">OUTPUTS</span></span>

### <span data-ttu-id="defff-136">PSLocationBasedServicesAccountKeys 中的 LocationBasedServices。</span><span class="sxs-lookup"><span data-stu-id="defff-136">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccountKeys</span></span>

### <span data-ttu-id="defff-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="defff-137">CommonParameters</span></span>
<span data-ttu-id="defff-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="defff-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="defff-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="defff-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="defff-140">筆記</span><span class="sxs-lookup"><span data-stu-id="defff-140">NOTES</span></span>

## <span data-ttu-id="defff-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="defff-141">RELATED LINKS</span></span>
