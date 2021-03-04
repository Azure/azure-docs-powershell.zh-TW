---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/new-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 0137a349408234f31f0002849230e023c0544f68
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910789"
---
# <span data-ttu-id="743ba-101">New-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="743ba-101">New-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="743ba-102">簡介</span><span class="sxs-lookup"><span data-stu-id="743ba-102">SYNOPSIS</span></span>
<span data-ttu-id="743ba-103">為應用程式深入資訊資源建立應用程式深入資訊 api 金鑰</span><span class="sxs-lookup"><span data-stu-id="743ba-103">Create an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="743ba-104">語法</span><span class="sxs-lookup"><span data-stu-id="743ba-104">SYNTAX</span></span>

### <span data-ttu-id="743ba-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="743ba-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="743ba-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="743ba-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="743ba-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="743ba-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="743ba-108">描述</span><span class="sxs-lookup"><span data-stu-id="743ba-108">DESCRIPTION</span></span>
<span data-ttu-id="743ba-109">為應用程式深入資訊資源建立應用程式深入資訊 api 鍵</span><span class="sxs-lookup"><span data-stu-id="743ba-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="743ba-110">例子</span><span class="sxs-lookup"><span data-stu-id="743ba-110">EXAMPLES</span></span>

### <span data-ttu-id="743ba-111">範例 1 為應用程式深入資訊資源建立新 Api 金鑰</span><span class="sxs-lookup"><span data-stu-id="743ba-111">Example 1 Create a new Api Key for an application insights resource</span></span>
```
PS C:\>$apiKeyDescription="testapiKey"
PS C:\>$permissions = @("ReadTelemetry", "WriteAnnotations")
PS C:\>New-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test" -Description $apiKeyDescription -Permissions $permissions

ApiKey      : st0rfelw7m3oimfspozrtwgccxihiftbdwqjdfkg
CreatedDate : Fri, 27 Oct 2017 16:59:19 GMT
Id          : 1ed593f9-1561-4981-922d-6917971eecd3
Permissions : {ReadTelemetry, WriteAnnotations}
Description : testapiKey
```

<span data-ttu-id="743ba-112">將應用程式深入資訊 api 金鑰描述建立為「testapiKey」，並擁有資源群組「testGroup」中資源「測試」的「ReadTelemetry」、「WriteAnnotations」等許可權。</span><span class="sxs-lookup"><span data-stu-id="743ba-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="743ba-113">參數</span><span class="sxs-lookup"><span data-stu-id="743ba-113">PARAMETERS</span></span>

### <span data-ttu-id="743ba-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="743ba-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="743ba-115">應用程式深入資訊元件物件。</span><span class="sxs-lookup"><span data-stu-id="743ba-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="743ba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="743ba-116">-DefaultProfile</span></span>
<span data-ttu-id="743ba-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="743ba-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="743ba-118">-描述</span><span class="sxs-lookup"><span data-stu-id="743ba-118">-Description</span></span>
<span data-ttu-id="743ba-119">說明，可協助識別此 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="743ba-119">Description to help identify this API key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="743ba-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="743ba-120">-Name</span></span>
<span data-ttu-id="743ba-121">元件名稱。</span><span class="sxs-lookup"><span data-stu-id="743ba-121">Component Name.</span></span>

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

### <span data-ttu-id="743ba-122">-許可權</span><span class="sxs-lookup"><span data-stu-id="743ba-122">-Permissions</span></span>
<span data-ttu-id="743ba-123">API 金鑰允許應用程式執行的許可權。</span><span class="sxs-lookup"><span data-stu-id="743ba-123">Permissions that API key allow apps to do.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ReadTelemetry, WriteAnnotations, AuthenticateSDKControlChannel

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="743ba-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="743ba-124">-ResourceGroupName</span></span>
<span data-ttu-id="743ba-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="743ba-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="743ba-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="743ba-126">-ResourceId</span></span>
<span data-ttu-id="743ba-127">應用程式深入資訊元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="743ba-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="743ba-128">-確認</span><span class="sxs-lookup"><span data-stu-id="743ba-128">-Confirm</span></span>
<span data-ttu-id="743ba-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="743ba-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="743ba-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="743ba-130">-WhatIf</span></span>
<span data-ttu-id="743ba-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="743ba-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="743ba-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="743ba-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="743ba-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="743ba-133">CommonParameters</span></span>
<span data-ttu-id="743ba-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="743ba-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="743ba-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="743ba-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="743ba-136">輸入</span><span class="sxs-lookup"><span data-stu-id="743ba-136">INPUTS</span></span>

### <span data-ttu-id="743ba-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="743ba-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="743ba-138">System.String</span><span class="sxs-lookup"><span data-stu-id="743ba-138">System.String</span></span>

## <span data-ttu-id="743ba-139">輸出</span><span class="sxs-lookup"><span data-stu-id="743ba-139">OUTPUTS</span></span>

### <span data-ttu-id="743ba-140">Microsoft.Azure.Commands.ApplicationInsights.models.PSApiKey</span><span class="sxs-lookup"><span data-stu-id="743ba-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="743ba-141">筆記</span><span class="sxs-lookup"><span data-stu-id="743ba-141">NOTES</span></span>

## <span data-ttu-id="743ba-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="743ba-142">RELATED LINKS</span></span>
