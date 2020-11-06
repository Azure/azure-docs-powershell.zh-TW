---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsApiKey.md
ms.openlocfilehash: bf5051f22d06e9e248501ecfb602bd47d3faaf39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613848"
---
# <span data-ttu-id="e1f16-101">Get-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="e1f16-101">Get-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="e1f16-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e1f16-102">SYNOPSIS</span></span>
<span data-ttu-id="e1f16-103">取得 application insights 資源的 application insights api 金鑰</span><span class="sxs-lookup"><span data-stu-id="e1f16-103">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="e1f16-104">句法</span><span class="sxs-lookup"><span data-stu-id="e1f16-104">SYNTAX</span></span>

### <span data-ttu-id="e1f16-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e1f16-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1f16-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1f16-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ApiKeyId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1f16-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1f16-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsApiKey [-ResourceId] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1f16-108">說明</span><span class="sxs-lookup"><span data-stu-id="e1f16-108">DESCRIPTION</span></span>
<span data-ttu-id="e1f16-109">取得 application insights 資源的 application insights api 金鑰</span><span class="sxs-lookup"><span data-stu-id="e1f16-109">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="e1f16-110">示例</span><span class="sxs-lookup"><span data-stu-id="e1f16-110">EXAMPLES</span></span>

### <span data-ttu-id="e1f16-111">範例1取得 application insights 資源的 Api 金鑰</span><span class="sxs-lookup"><span data-stu-id="e1f16-111">Example 1 Get Api Keys for an application insights resource</span></span>
```
PS C:\>  Get-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"

Id                                   Description Permissions                       CreatedDate                   ApiKey
--                                   ----------- -----------                       -----------                   ------
7c4c61dc-b392-4aa4-992f-ee92b84e5dee test1 ReadTelemetry                     Wed, 18 Oct 2017 23:36:40 GMT
63657030-dea6-4c52-82f4-6f5128cb92cb test2  {ReadTelemetry, WriteAnnotations} Wed, 18 Oct 2017 21:46:41 GMT
82549f39-f3ae-492e-8f94-f7aada75fa57 test3  ReadTelemetry                     Wed, 18 Oct 2017 22:30:23 GMT
```

<span data-ttu-id="e1f16-112">在資源群組 "testGroup" 中取得資源「test」的 application insights api 金鑰。</span><span class="sxs-lookup"><span data-stu-id="e1f16-112">Get application insights api keys for resource "test" in resource group "testGroup".</span></span>

### <span data-ttu-id="e1f16-113">範例2取得 application insights 資源的特定 API 金鑰</span><span class="sxs-lookup"><span data-stu-id="e1f16-113">Example 2 Get specific API key for an application insights resource</span></span>
```
PS C:\>  Get-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId 
7c4c61dc-b392-4aa4-992f-ee92b84e5dee
ApiKey      :
CreatedDate : Wed, 18 Oct 2017 23:36:40 GMT
Id          : 7c4c61dc-b392-4aa4-992f-ee92b84e5dee
Permissions : {ReadTelemetry}
Description : test1
```

<span data-ttu-id="e1f16-114">在資源群組 "9C29aa0f867" 中，取得 id 為 "dd173f38-4fd1-4c75-8af5-9 testGroup" 的特定 application insights api 金鑰。</span><span class="sxs-lookup"><span data-stu-id="e1f16-114">Get specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="e1f16-115">參數</span><span class="sxs-lookup"><span data-stu-id="e1f16-115">PARAMETERS</span></span>

### <span data-ttu-id="e1f16-116">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="e1f16-116">-ApiKeyId</span></span>
<span data-ttu-id="e1f16-117">Application Insights Api 金鑰識別碼。</span><span class="sxs-lookup"><span data-stu-id="e1f16-117">Application Insights Api Key Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f16-118">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="e1f16-118">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="e1f16-119">Application Insights 元件物件。</span><span class="sxs-lookup"><span data-stu-id="e1f16-119">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1f16-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1f16-120">-DefaultProfile</span></span>
<span data-ttu-id="e1f16-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e1f16-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1f16-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="e1f16-122">-Name</span></span>
<span data-ttu-id="e1f16-123">Application Insights 元件名稱。</span><span class="sxs-lookup"><span data-stu-id="e1f16-123">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f16-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1f16-124">-ResourceGroupName</span></span>
<span data-ttu-id="e1f16-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e1f16-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f16-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1f16-126">-ResourceId</span></span>
<span data-ttu-id="e1f16-127">Application Insights 元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e1f16-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="e1f16-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1f16-128">CommonParameters</span></span>
<span data-ttu-id="e1f16-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e1f16-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1f16-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e1f16-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1f16-131">輸入</span><span class="sxs-lookup"><span data-stu-id="e1f16-131">INPUTS</span></span>

### <span data-ttu-id="e1f16-132">PSApplicationInsightsComponent 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="e1f16-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="e1f16-133">System.object</span><span class="sxs-lookup"><span data-stu-id="e1f16-133">System.String</span></span>

## <span data-ttu-id="e1f16-134">輸出</span><span class="sxs-lookup"><span data-stu-id="e1f16-134">OUTPUTS</span></span>

### <span data-ttu-id="e1f16-135">PSApiKey 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="e1f16-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="e1f16-136">筆記</span><span class="sxs-lookup"><span data-stu-id="e1f16-136">NOTES</span></span>

## <span data-ttu-id="e1f16-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1f16-137">RELATED LINKS</span></span>
