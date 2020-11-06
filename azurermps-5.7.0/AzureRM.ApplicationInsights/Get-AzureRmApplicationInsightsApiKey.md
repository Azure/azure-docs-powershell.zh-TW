---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/get-azurermapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsApiKey.md
ms.openlocfilehash: 705ebfc151ef4f6bcd5029026ce08ee1da5bd676
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450751"
---
# <span data-ttu-id="95d0b-101">Get-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="95d0b-101">Get-AzureRmApplicationInsightsApiKey</span></span>

## <span data-ttu-id="95d0b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="95d0b-102">SYNOPSIS</span></span>
<span data-ttu-id="95d0b-103">取得 application insights 資源的 application insights api 金鑰</span><span class="sxs-lookup"><span data-stu-id="95d0b-103">Get application insights api keys for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95d0b-104">句法</span><span class="sxs-lookup"><span data-stu-id="95d0b-104">SYNTAX</span></span>

### <span data-ttu-id="95d0b-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="95d0b-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95d0b-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="95d0b-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ApiKeyId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95d0b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="95d0b-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmApplicationInsightsApiKey [-ResourceId] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95d0b-108">說明</span><span class="sxs-lookup"><span data-stu-id="95d0b-108">DESCRIPTION</span></span>
<span data-ttu-id="95d0b-109">取得 application insights 資源的 application insights api 金鑰</span><span class="sxs-lookup"><span data-stu-id="95d0b-109">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="95d0b-110">示例</span><span class="sxs-lookup"><span data-stu-id="95d0b-110">EXAMPLES</span></span>

### <span data-ttu-id="95d0b-111">範例1取得 application insights 資源的 Api 金鑰</span><span class="sxs-lookup"><span data-stu-id="95d0b-111">Example 1 Get Api Keys for an application insights resource</span></span>
```
PS C:\>  Get-AzureRmApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"

Id                                   Description Permissions                       CreatedDate                   ApiKey
--                                   ----------- -----------                       -----------                   ------
7c4c61dc-b392-4aa4-992f-ee92b84e5dee test1 ReadTelemetry                     Wed, 18 Oct 2017 23:36:40 GMT
63657030-dea6-4c52-82f4-6f5128cb92cb test2  {ReadTelemetry, WriteAnnotations} Wed, 18 Oct 2017 21:46:41 GMT
82549f39-f3ae-492e-8f94-f7aada75fa57 test3  ReadTelemetry                     Wed, 18 Oct 2017 22:30:23 GMT
```

<span data-ttu-id="95d0b-112">在資源群組 "testGroup" 中取得資源「test」的 application insights api 金鑰。</span><span class="sxs-lookup"><span data-stu-id="95d0b-112">Get application insights api keys for resource "test" in resource group "testGroup".</span></span>

### <span data-ttu-id="95d0b-113">範例2取得 application insights 資源的特定 API 金鑰</span><span class="sxs-lookup"><span data-stu-id="95d0b-113">Example 2 Get specific API key for an application insights resource</span></span>
```
PS C:\>  Get-AzureRmApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId 
7c4c61dc-b392-4aa4-992f-ee92b84e5dee
ApiKey      :
CreatedDate : Wed, 18 Oct 2017 23:36:40 GMT
Id          : 7c4c61dc-b392-4aa4-992f-ee92b84e5dee
Permissions : {ReadTelemetry}
Description : test1
```

<span data-ttu-id="95d0b-114">在資源群組 "9C29aa0f867" 中，取得 id 為 "dd173f38-4fd1-4c75-8af5-9 testGroup" 的特定 application insights api 金鑰。</span><span class="sxs-lookup"><span data-stu-id="95d0b-114">Get specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="95d0b-115">參數</span><span class="sxs-lookup"><span data-stu-id="95d0b-115">PARAMETERS</span></span>

### <span data-ttu-id="95d0b-116">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="95d0b-116">-ApiKeyId</span></span>
<span data-ttu-id="95d0b-117">Application Insights Api 金鑰識別碼。</span><span class="sxs-lookup"><span data-stu-id="95d0b-117">Application Insights Api Key Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d0b-118">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="95d0b-118">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="95d0b-119">Application Insights 元件物件。</span><span class="sxs-lookup"><span data-stu-id="95d0b-119">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95d0b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95d0b-120">-DefaultProfile</span></span>
<span data-ttu-id="95d0b-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="95d0b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95d0b-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="95d0b-122">-Name</span></span>
<span data-ttu-id="95d0b-123">Application Insights 元件名稱。</span><span class="sxs-lookup"><span data-stu-id="95d0b-123">Application Insights Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d0b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95d0b-124">-ResourceGroupName</span></span>
<span data-ttu-id="95d0b-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="95d0b-125">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d0b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95d0b-126">-ResourceId</span></span>
<span data-ttu-id="95d0b-127">Application Insights 元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="95d0b-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="95d0b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95d0b-128">CommonParameters</span></span>
<span data-ttu-id="95d0b-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="95d0b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95d0b-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="95d0b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95d0b-131">輸入</span><span class="sxs-lookup"><span data-stu-id="95d0b-131">INPUTS</span></span>

### <span data-ttu-id="95d0b-132">System.object</span><span class="sxs-lookup"><span data-stu-id="95d0b-132">System.String</span></span>

## <span data-ttu-id="95d0b-133">輸出</span><span class="sxs-lookup"><span data-stu-id="95d0b-133">OUTPUTS</span></span>

### <span data-ttu-id="95d0b-134">PSApiKey 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="95d0b-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="95d0b-135">筆記</span><span class="sxs-lookup"><span data-stu-id="95d0b-135">NOTES</span></span>

## <span data-ttu-id="95d0b-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="95d0b-136">RELATED LINKS</span></span>

