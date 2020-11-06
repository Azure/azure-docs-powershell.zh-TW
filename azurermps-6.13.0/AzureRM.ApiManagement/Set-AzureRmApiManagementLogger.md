---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
ms.openlocfilehash: 7a037b107f3d72a000c2f69c8de507a4f414e283
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448491"
---
# <span data-ttu-id="689b0-101">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="689b0-101">Set-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="689b0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="689b0-102">SYNOPSIS</span></span>
<span data-ttu-id="689b0-103">修改 API 記錄管理器。</span><span class="sxs-lookup"><span data-stu-id="689b0-103">Modifies an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="689b0-104">句法</span><span class="sxs-lookup"><span data-stu-id="689b0-104">SYNTAX</span></span>

### <span data-ttu-id="689b0-105">EventHubLoggerSet (預設) </span><span class="sxs-lookup"><span data-stu-id="689b0-105">EventHubLoggerSet (Default)</span></span>
```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="689b0-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="689b0-106">ApplicationInsightsLoggerSet</span></span>
```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-InstrumentationKey <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="689b0-107">說明</span><span class="sxs-lookup"><span data-stu-id="689b0-107">DESCRIPTION</span></span>
<span data-ttu-id="689b0-108">**AzureRmApiManagementLogger** Cmdlet 會修改 Azure API 管理 **記錄** 程式的設定。</span><span class="sxs-lookup"><span data-stu-id="689b0-108">The **Set-AzureRmApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="689b0-109">示例</span><span class="sxs-lookup"><span data-stu-id="689b0-109">EXAMPLES</span></span>

### <span data-ttu-id="689b0-110">範例1：修改 EventHub 記錄器</span><span class="sxs-lookup"><span data-stu-id="689b0-110">Example 1: Modify EventHub logger</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="689b0-111">這個命令會修改 ID 為 Logger123 的記錄器。</span><span class="sxs-lookup"><span data-stu-id="689b0-111">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="689b0-112">參數</span><span class="sxs-lookup"><span data-stu-id="689b0-112">PARAMETERS</span></span>

### <span data-ttu-id="689b0-113">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="689b0-113">-ConnectionString</span></span>
<span data-ttu-id="689b0-114">指定包含傳送原則許可權的 Azure 事件中心連線字串。</span><span class="sxs-lookup"><span data-stu-id="689b0-114">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="689b0-115">-內容</span><span class="sxs-lookup"><span data-stu-id="689b0-115">-Context</span></span>
<span data-ttu-id="689b0-116">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="689b0-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="689b0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="689b0-117">-DefaultProfile</span></span>
<span data-ttu-id="689b0-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="689b0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="689b0-119">-描述</span><span class="sxs-lookup"><span data-stu-id="689b0-119">-Description</span></span>
<span data-ttu-id="689b0-120">指定描述。</span><span class="sxs-lookup"><span data-stu-id="689b0-120">Specifies a description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="689b0-121">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="689b0-121">-InstrumentationKey</span></span>
<span data-ttu-id="689b0-122">Application Insights 的工具金鑰。</span><span class="sxs-lookup"><span data-stu-id="689b0-122">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="689b0-123">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="689b0-123">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationInsightsLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="689b0-124">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="689b0-124">-IsBuffered</span></span>
<span data-ttu-id="689b0-125">指定在發佈前先緩衝記錄器中的記錄。</span><span class="sxs-lookup"><span data-stu-id="689b0-125">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="689b0-126">當記錄經過緩衝處理時，會每隔15秒傳送給事件中心，或每當緩衝區收到 256 KB 的訊息。</span><span class="sxs-lookup"><span data-stu-id="689b0-126">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="689b0-127">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="689b0-127">-LoggerId</span></span>
<span data-ttu-id="689b0-128">指定要更新的記錄器識別碼。</span><span class="sxs-lookup"><span data-stu-id="689b0-128">Specifies the ID of the logger to update.</span></span>

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

### <span data-ttu-id="689b0-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="689b0-129">-Name</span></span>
<span data-ttu-id="689b0-130">從 Azure 傳統入口網站指定事件中心的機構名稱。</span><span class="sxs-lookup"><span data-stu-id="689b0-130">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="689b0-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="689b0-131">-PassThru</span></span>
<span data-ttu-id="689b0-132">指示這個 Cmdlet 會傳回這個 Cmdlet 修改的  **PsApiManagementLogger** 。</span><span class="sxs-lookup"><span data-stu-id="689b0-132">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="689b0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="689b0-133">CommonParameters</span></span>
<span data-ttu-id="689b0-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="689b0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="689b0-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="689b0-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="689b0-136">輸入</span><span class="sxs-lookup"><span data-stu-id="689b0-136">INPUTS</span></span>

### <span data-ttu-id="689b0-137">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="689b0-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="689b0-138">System.object</span><span class="sxs-lookup"><span data-stu-id="689b0-138">System.String</span></span>

### <span data-ttu-id="689b0-139">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="689b0-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="689b0-140">輸出</span><span class="sxs-lookup"><span data-stu-id="689b0-140">OUTPUTS</span></span>

### <span data-ttu-id="689b0-141">ServiceManagement. PsApiManagementLogger （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="689b0-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="689b0-142">筆記</span><span class="sxs-lookup"><span data-stu-id="689b0-142">NOTES</span></span>

## <span data-ttu-id="689b0-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="689b0-143">RELATED LINKS</span></span>

[<span data-ttu-id="689b0-144">AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="689b0-144">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="689b0-145">新-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="689b0-145">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="689b0-146">移除-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="689b0-146">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)


