---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/get-azurermmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccountKey.md
ms.openlocfilehash: 1afe0f8f93bd00a384e1bb741ed8ea54e1ae66d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449758"
---
# <span data-ttu-id="fb515-101">Get-AzureRmMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="fb515-101">Get-AzureRmMapsAccountKey</span></span>

## <span data-ttu-id="fb515-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fb515-102">SYNOPSIS</span></span>
<span data-ttu-id="fb515-103">取得帳戶的 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="fb515-103">Gets the API keys for an account.</span></span>
<span data-ttu-id="fb515-104">這些金鑰是在對 Azure 對應進行後續呼叫時所使用的驗證機制。</span><span class="sxs-lookup"><span data-stu-id="fb515-104">These keys are the authentication mechanism used in subsequent calls to Azure Maps.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb515-105">句法</span><span class="sxs-lookup"><span data-stu-id="fb515-105">SYNTAX</span></span>

### <span data-ttu-id="fb515-106">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fb515-106">NameParameterSet (Default)</span></span>
```
Get-AzureRmMapsAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb515-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb515-107">InputObjectParameterSet</span></span>
```
Get-AzureRmMapsAccountKey [-InputObject <PSMapsAccount>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fb515-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb515-108">ResourceIdParameterSet</span></span>
```
Get-AzureRmMapsAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb515-109">說明</span><span class="sxs-lookup"><span data-stu-id="fb515-109">DESCRIPTION</span></span>
<span data-ttu-id="fb515-110">Get-AzureRmMapsAccountKey Cmdlet 會取得已置備之 Azure 地圖帳戶的 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="fb515-110">The Get-AzureRmMapsAccountKey cmdlet gets the API keys for a provisioned Azure Maps account.</span></span>
<span data-ttu-id="fb515-111">Azure 地圖帳戶有兩個 API 金鑰：主要和次要。</span><span class="sxs-lookup"><span data-stu-id="fb515-111">An Azure Maps account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="fb515-112">這些金鑰可讓您與 Azure Maps 帳戶端點互動。</span><span class="sxs-lookup"><span data-stu-id="fb515-112">The keys enable interaction with the Azure Maps account endpoint.</span></span>
<span data-ttu-id="fb515-113">使用 New-AzureRmMapsAccountKey (New-AzureRmMapsAccountKey.md) 重新產生金鑰。</span><span class="sxs-lookup"><span data-stu-id="fb515-113">Use New-AzureRmMapsAccountKey (New-AzureRmMapsAccountKey.md)to regenerate a key.</span></span>

## <span data-ttu-id="fb515-114">示例</span><span class="sxs-lookup"><span data-stu-id="fb515-114">EXAMPLES</span></span>

### <span data-ttu-id="fb515-115">範例1</span><span class="sxs-lookup"><span data-stu-id="fb515-115">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="fb515-116">傳回 [資源群組 MyResourceGroup] 中名為 [我的帳戶] 的帳戶按鍵。</span><span class="sxs-lookup"><span data-stu-id="fb515-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="fb515-117">範例2</span><span class="sxs-lookup"><span data-stu-id="fb515-117">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="fb515-118">傳回指定 Azure Maps 帳戶的按鍵。</span><span class="sxs-lookup"><span data-stu-id="fb515-118">Returns the keys for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="fb515-119">參數</span><span class="sxs-lookup"><span data-stu-id="fb515-119">PARAMETERS</span></span>

### <span data-ttu-id="fb515-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb515-120">-DefaultProfile</span></span>
<span data-ttu-id="fb515-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fb515-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb515-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb515-122">-InputObject</span></span>
<span data-ttu-id="fb515-123">從 AzureRmMapsAccount 將 [地圖] 帳戶成管道。</span><span class="sxs-lookup"><span data-stu-id="fb515-123">Maps Account piped from Get-AzureRmMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb515-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="fb515-124">-Name</span></span>
<span data-ttu-id="fb515-125">地圖帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="fb515-125">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb515-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb515-126">-ResourceGroupName</span></span>
<span data-ttu-id="fb515-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="fb515-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb515-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb515-128">-ResourceId</span></span>
<span data-ttu-id="fb515-129">地圖帳戶 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="fb515-129">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb515-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb515-130">CommonParameters</span></span>
<span data-ttu-id="fb515-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fb515-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb515-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fb515-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb515-133">輸入</span><span class="sxs-lookup"><span data-stu-id="fb515-133">INPUTS</span></span>

### <span data-ttu-id="fb515-134">System.object</span><span class="sxs-lookup"><span data-stu-id="fb515-134">System.String</span></span>

### <span data-ttu-id="fb515-135">PSMapsAccount 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fb515-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>
<span data-ttu-id="fb515-136">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="fb515-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="fb515-137">輸出</span><span class="sxs-lookup"><span data-stu-id="fb515-137">OUTPUTS</span></span>

### <span data-ttu-id="fb515-138">PSMapsAccountKeys 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fb515-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span></span>

## <span data-ttu-id="fb515-139">筆記</span><span class="sxs-lookup"><span data-stu-id="fb515-139">NOTES</span></span>

## <span data-ttu-id="fb515-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb515-140">RELATED LINKS</span></span>
