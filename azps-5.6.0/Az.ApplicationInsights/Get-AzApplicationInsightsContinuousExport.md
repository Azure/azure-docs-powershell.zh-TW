---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/get-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 63c31e07313f7e6ad3e1eea25977e85f3e4c6b53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905233"
---
# <span data-ttu-id="9eca7-101">Get-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="9eca7-101">Get-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="9eca7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9eca7-102">SYNOPSIS</span></span>
<span data-ttu-id="9eca7-103">取得應用程式深入資訊連續匯出設定檔的應用程式深入資訊資源</span><span class="sxs-lookup"><span data-stu-id="9eca7-103">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="9eca7-104">語法</span><span class="sxs-lookup"><span data-stu-id="9eca7-104">SYNTAX</span></span>

### <span data-ttu-id="9eca7-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9eca7-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9eca7-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9eca7-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9eca7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9eca7-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceId] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9eca7-108">描述</span><span class="sxs-lookup"><span data-stu-id="9eca7-108">DESCRIPTION</span></span>
<span data-ttu-id="9eca7-109">取得應用程式深入資訊連續匯出設定檔的應用程式深入資訊資源</span><span class="sxs-lookup"><span data-stu-id="9eca7-109">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="9eca7-110">例子</span><span class="sxs-lookup"><span data-stu-id="9eca7-110">EXAMPLES</span></span>

### <span data-ttu-id="9eca7-111">範例 1 取得應用程式深入資訊資源的連續匯出</span><span class="sxs-lookup"><span data-stu-id="9eca7-111">Example 1 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"

ExportId                     DocumentTypes                ExportStatus DestinationStorageAccountId
--------                     -------------                ------------ ---------------------------
ZJrfffySPdtG3ESn3iRxVIEFuNY= Request, Performance Counter Preparing    /subscriptions/{subid}...
```

<span data-ttu-id="9eca7-112">在資源群組"testgroup" 中取得資源名為"test" 的應用程式深入資訊連續匯出組</span><span class="sxs-lookup"><span data-stu-id="9eca7-112">Get application insights continuous export configurations for resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="9eca7-113">範例 2 取得應用程式深入資訊資源的連續匯出</span><span class="sxs-lookup"><span data-stu-id="9eca7-113">Example 2 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "ZJrfffySPdtG3ESn3iRxVIEFuNY="

ExportId                         : ZJrfffySPdtG3ESn3iRxVIEFuNY=
StorageName                      : targetaccount
ContainerName                    : continuousexport
DocumentTypes                    : Request, Performance Counter
DestinationStorageSubscriptionId : {subid}
DestinationStorageLocationId     : eastus
DestinationStorageAccountId      : /subscriptions/{subid}/resourceGroups/targetstorage/providers/Microsoft.Storage/storageAccounts/targetaccount
IsEnabled                        : True
ExportStatus                     : Preparing
LastSuccessTime                  :
```

<span data-ttu-id="9eca7-114">使用匯出識別碼 "ZJrfffySPdtG3ESn3iRx區FuNY=" 取得應用程式深入資訊連續匯出組，用於資源群組 "testgroup" 中名為 "test" 的資源</span><span class="sxs-lookup"><span data-stu-id="9eca7-114">Get application insights continuous export configuration with export id "ZJrfffySPdtG3ESn3iRxVIEFuNY=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="9eca7-115">參數</span><span class="sxs-lookup"><span data-stu-id="9eca7-115">PARAMETERS</span></span>

### <span data-ttu-id="9eca7-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="9eca7-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="9eca7-117">應用程式深入資訊元件物件。</span><span class="sxs-lookup"><span data-stu-id="9eca7-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="9eca7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eca7-118">-DefaultProfile</span></span>
<span data-ttu-id="9eca7-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9eca7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9eca7-120">-ExportId</span><span class="sxs-lookup"><span data-stu-id="9eca7-120">-ExportId</span></span>
<span data-ttu-id="9eca7-121">應用程式深入資訊連續匯出識別碼。</span><span class="sxs-lookup"><span data-stu-id="9eca7-121">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="9eca7-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="9eca7-122">-Name</span></span>
<span data-ttu-id="9eca7-123">應用程式深入資訊元件名稱。</span><span class="sxs-lookup"><span data-stu-id="9eca7-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="9eca7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eca7-124">-ResourceGroupName</span></span>
<span data-ttu-id="9eca7-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="9eca7-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="9eca7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9eca7-126">-ResourceId</span></span>
<span data-ttu-id="9eca7-127">應用程式深入資訊元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9eca7-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="9eca7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eca7-128">CommonParameters</span></span>
<span data-ttu-id="9eca7-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9eca7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eca7-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="9eca7-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eca7-131">輸入</span><span class="sxs-lookup"><span data-stu-id="9eca7-131">INPUTS</span></span>

### <span data-ttu-id="9eca7-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="9eca7-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="9eca7-133">System.String</span><span class="sxs-lookup"><span data-stu-id="9eca7-133">System.String</span></span>

## <span data-ttu-id="9eca7-134">輸出</span><span class="sxs-lookup"><span data-stu-id="9eca7-134">OUTPUTS</span></span>

### <span data-ttu-id="9eca7-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="9eca7-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="9eca7-136">筆記</span><span class="sxs-lookup"><span data-stu-id="9eca7-136">NOTES</span></span>

## <span data-ttu-id="9eca7-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="9eca7-137">RELATED LINKS</span></span>
