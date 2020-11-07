---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
ms.openlocfilehash: 6ad32b3bd9bef4f4e684125b280db941da7a7b3f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965626"
---
# <span data-ttu-id="61614-101">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="61614-101">Set-AzApiManagementLogger</span></span>

## <span data-ttu-id="61614-102">摘要</span><span class="sxs-lookup"><span data-stu-id="61614-102">SYNOPSIS</span></span>
<span data-ttu-id="61614-103">修改 API 記錄管理器。</span><span class="sxs-lookup"><span data-stu-id="61614-103">Modifies an API Management Logger.</span></span>

## <span data-ttu-id="61614-104">句法</span><span class="sxs-lookup"><span data-stu-id="61614-104">SYNTAX</span></span>

### <span data-ttu-id="61614-105">EventHubLoggerSet (預設) </span><span class="sxs-lookup"><span data-stu-id="61614-105">EventHubLoggerSet (Default)</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61614-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="61614-106">ApplicationInsightsLoggerSet</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-InstrumentationKey <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61614-107">說明</span><span class="sxs-lookup"><span data-stu-id="61614-107">DESCRIPTION</span></span>
<span data-ttu-id="61614-108">**AzApiManagementLogger** Cmdlet 會修改 Azure API 管理 **記錄** 程式的設定。</span><span class="sxs-lookup"><span data-stu-id="61614-108">The **Set-AzApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="61614-109">示例</span><span class="sxs-lookup"><span data-stu-id="61614-109">EXAMPLES</span></span>

### <span data-ttu-id="61614-110">範例1：修改 EventHub 記錄器</span><span class="sxs-lookup"><span data-stu-id="61614-110">Example 1: Modify EventHub logger</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="61614-111">這個命令會修改 ID 為 Logger123 的記錄器。</span><span class="sxs-lookup"><span data-stu-id="61614-111">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="61614-112">參數</span><span class="sxs-lookup"><span data-stu-id="61614-112">PARAMETERS</span></span>

### <span data-ttu-id="61614-113">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="61614-113">-ConnectionString</span></span>
<span data-ttu-id="61614-114">指定包含傳送原則許可權的 Azure 事件中心連線字串。</span><span class="sxs-lookup"><span data-stu-id="61614-114">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

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

### <span data-ttu-id="61614-115">-內容</span><span class="sxs-lookup"><span data-stu-id="61614-115">-Context</span></span>
<span data-ttu-id="61614-116">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="61614-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61614-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61614-117">-DefaultProfile</span></span>
<span data-ttu-id="61614-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="61614-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61614-119">-描述</span><span class="sxs-lookup"><span data-stu-id="61614-119">-Description</span></span>
<span data-ttu-id="61614-120">指定描述。</span><span class="sxs-lookup"><span data-stu-id="61614-120">Specifies a description.</span></span>

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

### <span data-ttu-id="61614-121">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="61614-121">-InstrumentationKey</span></span>
<span data-ttu-id="61614-122">Application Insights 的工具金鑰。</span><span class="sxs-lookup"><span data-stu-id="61614-122">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="61614-123">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="61614-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="61614-124">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="61614-124">-IsBuffered</span></span>
<span data-ttu-id="61614-125">指定在發佈前先緩衝記錄器中的記錄。</span><span class="sxs-lookup"><span data-stu-id="61614-125">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="61614-126">當記錄經過緩衝處理時，會每隔15秒傳送給事件中心，或每當緩衝區收到 256 KB 的訊息。</span><span class="sxs-lookup"><span data-stu-id="61614-126">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

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

### <span data-ttu-id="61614-127">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="61614-127">-LoggerId</span></span>
<span data-ttu-id="61614-128">指定要更新的記錄器識別碼。</span><span class="sxs-lookup"><span data-stu-id="61614-128">Specifies the ID of the logger to update.</span></span>

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

### <span data-ttu-id="61614-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="61614-129">-Name</span></span>
<span data-ttu-id="61614-130">從 Azure 傳統入口網站指定事件中心的機構名稱。</span><span class="sxs-lookup"><span data-stu-id="61614-130">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="61614-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61614-131">-PassThru</span></span>
<span data-ttu-id="61614-132">指示這個 Cmdlet 會傳回這個 Cmdlet 修改的  **PsApiManagementLogger** 。</span><span class="sxs-lookup"><span data-stu-id="61614-132">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="61614-133">-確認</span><span class="sxs-lookup"><span data-stu-id="61614-133">-Confirm</span></span>
<span data-ttu-id="61614-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="61614-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61614-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61614-135">-WhatIf</span></span>
<span data-ttu-id="61614-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="61614-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61614-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="61614-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61614-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61614-138">CommonParameters</span></span>
<span data-ttu-id="61614-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="61614-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61614-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="61614-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61614-141">輸入</span><span class="sxs-lookup"><span data-stu-id="61614-141">INPUTS</span></span>

### <span data-ttu-id="61614-142">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="61614-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="61614-143">System.object</span><span class="sxs-lookup"><span data-stu-id="61614-143">System.String</span></span>

### <span data-ttu-id="61614-144">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="61614-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="61614-145">輸出</span><span class="sxs-lookup"><span data-stu-id="61614-145">OUTPUTS</span></span>

### <span data-ttu-id="61614-146">ServiceManagement. PsApiManagementLogger （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="61614-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="61614-147">筆記</span><span class="sxs-lookup"><span data-stu-id="61614-147">NOTES</span></span>

## <span data-ttu-id="61614-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="61614-148">RELATED LINKS</span></span>

[<span data-ttu-id="61614-149">AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="61614-149">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="61614-150">新-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="61614-150">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="61614-151">移除-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="61614-151">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)


