---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/get-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: 5e3b2feff3b59df30960856718911a3aeb699c37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450747"
---
# <span data-ttu-id="1d76a-101">Get-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="1d76a-101">Get-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="1d76a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1d76a-102">SYNOPSIS</span></span>
<span data-ttu-id="1d76a-103">取得 application insights 資源的 application insights 連續匯出配置</span><span class="sxs-lookup"><span data-stu-id="1d76a-103">Get application insights continuous export configuration for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d76a-104">句法</span><span class="sxs-lookup"><span data-stu-id="1d76a-104">SYNTAX</span></span>

### <span data-ttu-id="1d76a-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1d76a-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d76a-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d76a-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d76a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d76a-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d76a-108">說明</span><span class="sxs-lookup"><span data-stu-id="1d76a-108">DESCRIPTION</span></span>
<span data-ttu-id="1d76a-109">取得 application insights 資源的 application insights 連續匯出配置</span><span class="sxs-lookup"><span data-stu-id="1d76a-109">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="1d76a-110">示例</span><span class="sxs-lookup"><span data-stu-id="1d76a-110">EXAMPLES</span></span>

### <span data-ttu-id="1d76a-111">範例1取得 application insights 資源的連續匯出</span><span class="sxs-lookup"><span data-stu-id="1d76a-111">Example 1 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"

ExportId                     DocumentTypes                ExportStatus DestinationStorageAccountId
--------                     -------------                ------------ ---------------------------
ZJrfffySPdtG3ESn3iRxVIEFuNY= Request, Performance Counter Preparing    /subscriptions/{subid}...
```

<span data-ttu-id="1d76a-112">在資源群組 "testgroup" 中取得名為「test」之資源的 application insights 連續匯出設定</span><span class="sxs-lookup"><span data-stu-id="1d76a-112">Get application insights continuous export configurations for resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="1d76a-113">範例2取得 application insights 資源的連續匯出</span><span class="sxs-lookup"><span data-stu-id="1d76a-113">Example 2 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "ZJrfffySPdtG3ESn3iRxVIEFuNY="

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

<span data-ttu-id="1d76a-114">針對資源群組 "testgroup" 中名為 "test" 的資源，取得含匯出 id "ZJrfffySPdtG3ESn3iRxVIEFuNY =" 的 application insights 連續匯出設定</span><span class="sxs-lookup"><span data-stu-id="1d76a-114">Get application insights continuous export configuration with export id "ZJrfffySPdtG3ESn3iRxVIEFuNY=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="1d76a-115">參數</span><span class="sxs-lookup"><span data-stu-id="1d76a-115">PARAMETERS</span></span>

### <span data-ttu-id="1d76a-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="1d76a-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="1d76a-117">Application Insights 元件物件。</span><span class="sxs-lookup"><span data-stu-id="1d76a-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="1d76a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d76a-118">-DefaultProfile</span></span>
<span data-ttu-id="1d76a-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1d76a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d76a-120">-ExportId</span><span class="sxs-lookup"><span data-stu-id="1d76a-120">-ExportId</span></span>
<span data-ttu-id="1d76a-121">Application Insights 連續匯出 Id。</span><span class="sxs-lookup"><span data-stu-id="1d76a-121">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="1d76a-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="1d76a-122">-Name</span></span>
<span data-ttu-id="1d76a-123">Application Insights 元件名稱。</span><span class="sxs-lookup"><span data-stu-id="1d76a-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="1d76a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d76a-124">-ResourceGroupName</span></span>
<span data-ttu-id="1d76a-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="1d76a-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="1d76a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d76a-126">-ResourceId</span></span>
<span data-ttu-id="1d76a-127">Application Insights 元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1d76a-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="1d76a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d76a-128">CommonParameters</span></span>
<span data-ttu-id="1d76a-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1d76a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d76a-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1d76a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d76a-131">輸入</span><span class="sxs-lookup"><span data-stu-id="1d76a-131">INPUTS</span></span>

### <span data-ttu-id="1d76a-132">System.object</span><span class="sxs-lookup"><span data-stu-id="1d76a-132">System.String</span></span>

## <span data-ttu-id="1d76a-133">輸出</span><span class="sxs-lookup"><span data-stu-id="1d76a-133">OUTPUTS</span></span>

### <span data-ttu-id="1d76a-134">PSExportConfiguration 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="1d76a-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="1d76a-135">筆記</span><span class="sxs-lookup"><span data-stu-id="1d76a-135">NOTES</span></span>

## <span data-ttu-id="1d76a-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="1d76a-136">RELATED LINKS</span></span>

