---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/new-azurermapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsApiKey.md
ms.openlocfilehash: 4c7f488e7a9ffca823128cccff18ba33b88dabfd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450740"
---
# <span data-ttu-id="c46b0-101">New-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="c46b0-101">New-AzureRmApplicationInsightsApiKey</span></span>

## <span data-ttu-id="c46b0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c46b0-102">SYNOPSIS</span></span>
<span data-ttu-id="c46b0-103">建立 application insights 資源的 application insights api 金鑰</span><span class="sxs-lookup"><span data-stu-id="c46b0-103">Create an application insights api key for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c46b0-104">句法</span><span class="sxs-lookup"><span data-stu-id="c46b0-104">SYNTAX</span></span>

### <span data-ttu-id="c46b0-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c46b0-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c46b0-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c46b0-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c46b0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c46b0-107">ResourceIdParameterSet</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c46b0-108">說明</span><span class="sxs-lookup"><span data-stu-id="c46b0-108">DESCRIPTION</span></span>
<span data-ttu-id="c46b0-109">為 application insights 資源建立 application insights api 金鑰</span><span class="sxs-lookup"><span data-stu-id="c46b0-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="c46b0-110">示例</span><span class="sxs-lookup"><span data-stu-id="c46b0-110">EXAMPLES</span></span>

### <span data-ttu-id="c46b0-111">範例1為 application insights 資源建立新的 Api 金鑰</span><span class="sxs-lookup"><span data-stu-id="c46b0-111">Example 1 Create a new Api Key for an application insights resource</span></span>
```
PS C:\>$apiKeyDescription="testapiKey"
PS C:\>$permissions = @("ReadTelemetry", "WriteAnnotations")
PS C:\>New-AzureRmApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test" -Description $apiKeyDescription -Permissions $permissions

ApiKey      : st0rfelw7m3oimfspozrtwgccxihiftbdwqjdfkg
CreatedDate : Fri, 27 Oct 2017 16:59:19 GMT
Id          : 1ed593f9-1561-4981-922d-6917971eecd3
Permissions : {ReadTelemetry, WriteAnnotations}
Description : testapiKey
```

<span data-ttu-id="c46b0-112">在資源群組 "testGroup" 中，建立 application insights api 金鑰描述為「testapiKey」，並包含許可權為「ReadTelemetry」，"WriteAnnotations" 資源 "test"。</span><span class="sxs-lookup"><span data-stu-id="c46b0-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="c46b0-113">參數</span><span class="sxs-lookup"><span data-stu-id="c46b0-113">PARAMETERS</span></span>

### <span data-ttu-id="c46b0-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c46b0-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="c46b0-115">Application Insights 元件物件。</span><span class="sxs-lookup"><span data-stu-id="c46b0-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="c46b0-116">-確認</span><span class="sxs-lookup"><span data-stu-id="c46b0-116">-Confirm</span></span>
<span data-ttu-id="c46b0-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c46b0-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c46b0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c46b0-118">-DefaultProfile</span></span>
<span data-ttu-id="c46b0-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c46b0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c46b0-120">-描述</span><span class="sxs-lookup"><span data-stu-id="c46b0-120">-Description</span></span>
<span data-ttu-id="c46b0-121">說明以協助識別這個 API 金鑰的描述。</span><span class="sxs-lookup"><span data-stu-id="c46b0-121">Description to help identify this API key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46b0-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="c46b0-122">-Name</span></span>
<span data-ttu-id="c46b0-123">元件名稱。</span><span class="sxs-lookup"><span data-stu-id="c46b0-123">Component Name.</span></span>

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

### <span data-ttu-id="c46b0-124">-許可權</span><span class="sxs-lookup"><span data-stu-id="c46b0-124">-Permissions</span></span>
<span data-ttu-id="c46b0-125">API 金鑰允許 app 執行的許可權。</span><span class="sxs-lookup"><span data-stu-id="c46b0-125">Permissions that API key allow apps to do.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Accepted values: ReadTelemetry, WriteAnnotations, AuthenticateSDKControlChannel

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46b0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c46b0-126">-ResourceGroupName</span></span>
<span data-ttu-id="c46b0-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c46b0-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="c46b0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c46b0-128">-ResourceId</span></span>
<span data-ttu-id="c46b0-129">Application Insights 元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c46b0-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="c46b0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c46b0-130">-WhatIf</span></span>
<span data-ttu-id="c46b0-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c46b0-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c46b0-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c46b0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c46b0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c46b0-133">CommonParameters</span></span>
<span data-ttu-id="c46b0-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c46b0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c46b0-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c46b0-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c46b0-136">輸入</span><span class="sxs-lookup"><span data-stu-id="c46b0-136">INPUTS</span></span>

### <span data-ttu-id="c46b0-137">System.object</span><span class="sxs-lookup"><span data-stu-id="c46b0-137">System.String</span></span>
<span data-ttu-id="c46b0-138">System.object []</span><span class="sxs-lookup"><span data-stu-id="c46b0-138">System.String[]</span></span>

## <span data-ttu-id="c46b0-139">輸出</span><span class="sxs-lookup"><span data-stu-id="c46b0-139">OUTPUTS</span></span>

### <span data-ttu-id="c46b0-140">PSApiKey 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="c46b0-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="c46b0-141">筆記</span><span class="sxs-lookup"><span data-stu-id="c46b0-141">NOTES</span></span>

## <span data-ttu-id="c46b0-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="c46b0-142">RELATED LINKS</span></span>

