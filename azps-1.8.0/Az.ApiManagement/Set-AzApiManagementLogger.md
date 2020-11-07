---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
ms.openlocfilehash: 4c7f4b4f308d04c6f9c82e70f9fbe0598bd4a9fb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788758"
---
# <span data-ttu-id="8d619-101">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="8d619-101">Set-AzApiManagementLogger</span></span>

## <span data-ttu-id="8d619-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8d619-102">SYNOPSIS</span></span>
<span data-ttu-id="8d619-103">修改 API 記錄管理器。</span><span class="sxs-lookup"><span data-stu-id="8d619-103">Modifies an API Management Logger.</span></span>

## <span data-ttu-id="8d619-104">句法</span><span class="sxs-lookup"><span data-stu-id="8d619-104">SYNTAX</span></span>

### <span data-ttu-id="8d619-105">EventHubLoggerSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8d619-105">EventHubLoggerSet (Default)</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d619-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="8d619-106">ApplicationInsightsLoggerSet</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-InstrumentationKey <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d619-107">說明</span><span class="sxs-lookup"><span data-stu-id="8d619-107">DESCRIPTION</span></span>
<span data-ttu-id="8d619-108">**AzApiManagementLogger** Cmdlet 會修改 Azure API 管理 **記錄** 程式的設定。</span><span class="sxs-lookup"><span data-stu-id="8d619-108">The **Set-AzApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="8d619-109">示例</span><span class="sxs-lookup"><span data-stu-id="8d619-109">EXAMPLES</span></span>

### <span data-ttu-id="8d619-110">範例1：修改 EventHub 記錄器</span><span class="sxs-lookup"><span data-stu-id="8d619-110">Example 1: Modify EventHub logger</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="8d619-111">這個命令會修改 ID 為 Logger123 的記錄器。</span><span class="sxs-lookup"><span data-stu-id="8d619-111">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="8d619-112">參數</span><span class="sxs-lookup"><span data-stu-id="8d619-112">PARAMETERS</span></span>

### <span data-ttu-id="8d619-113">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="8d619-113">-ConnectionString</span></span>
<span data-ttu-id="8d619-114">指定包含傳送原則許可權的 Azure 事件中心連線字串。</span><span class="sxs-lookup"><span data-stu-id="8d619-114">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

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

### <span data-ttu-id="8d619-115">-內容</span><span class="sxs-lookup"><span data-stu-id="8d619-115">-Context</span></span>
<span data-ttu-id="8d619-116">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="8d619-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8d619-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d619-117">-DefaultProfile</span></span>
<span data-ttu-id="8d619-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8d619-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d619-119">-描述</span><span class="sxs-lookup"><span data-stu-id="8d619-119">-Description</span></span>
<span data-ttu-id="8d619-120">指定描述。</span><span class="sxs-lookup"><span data-stu-id="8d619-120">Specifies a description.</span></span>

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

### <span data-ttu-id="8d619-121">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="8d619-121">-InstrumentationKey</span></span>
<span data-ttu-id="8d619-122">Application Insights 的工具金鑰。</span><span class="sxs-lookup"><span data-stu-id="8d619-122">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="8d619-123">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="8d619-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="8d619-124">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="8d619-124">-IsBuffered</span></span>
<span data-ttu-id="8d619-125">指定在發佈前先緩衝記錄器中的記錄。</span><span class="sxs-lookup"><span data-stu-id="8d619-125">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="8d619-126">當記錄經過緩衝處理時，會每隔15秒傳送給事件中心，或每當緩衝區收到 256 KB 的訊息。</span><span class="sxs-lookup"><span data-stu-id="8d619-126">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

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

### <span data-ttu-id="8d619-127">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="8d619-127">-LoggerId</span></span>
<span data-ttu-id="8d619-128">指定要更新的記錄器識別碼。</span><span class="sxs-lookup"><span data-stu-id="8d619-128">Specifies the ID of the logger to update.</span></span>

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

### <span data-ttu-id="8d619-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="8d619-129">-Name</span></span>
<span data-ttu-id="8d619-130">從 Azure 傳統入口網站指定事件中心的機構名稱。</span><span class="sxs-lookup"><span data-stu-id="8d619-130">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="8d619-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d619-131">-PassThru</span></span>
<span data-ttu-id="8d619-132">指示這個 Cmdlet 會傳回這個 Cmdlet 修改的  **PsApiManagementLogger** 。</span><span class="sxs-lookup"><span data-stu-id="8d619-132">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8d619-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d619-133">CommonParameters</span></span>
<span data-ttu-id="8d619-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8d619-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d619-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8d619-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d619-136">輸入</span><span class="sxs-lookup"><span data-stu-id="8d619-136">INPUTS</span></span>

### <span data-ttu-id="8d619-137">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="8d619-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8d619-138">System.object</span><span class="sxs-lookup"><span data-stu-id="8d619-138">System.String</span></span>

### <span data-ttu-id="8d619-139">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="8d619-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8d619-140">輸出</span><span class="sxs-lookup"><span data-stu-id="8d619-140">OUTPUTS</span></span>

### <span data-ttu-id="8d619-141">ServiceManagement. PsApiManagementLogger （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="8d619-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="8d619-142">筆記</span><span class="sxs-lookup"><span data-stu-id="8d619-142">NOTES</span></span>

## <span data-ttu-id="8d619-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d619-143">RELATED LINKS</span></span>

[<span data-ttu-id="8d619-144">AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="8d619-144">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="8d619-145">新-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="8d619-145">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="8d619-146">移除-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="8d619-146">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)


