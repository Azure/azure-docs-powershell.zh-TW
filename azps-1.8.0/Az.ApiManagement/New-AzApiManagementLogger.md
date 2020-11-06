---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementLogger.md
ms.openlocfilehash: 3df5f6974cd955035c16972a5a7358aa44a30390
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93623116"
---
# <span data-ttu-id="be1c2-101">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="be1c2-101">New-AzApiManagementLogger</span></span>

## <span data-ttu-id="be1c2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="be1c2-102">SYNOPSIS</span></span>
<span data-ttu-id="be1c2-103">建立 API 記錄管理器。</span><span class="sxs-lookup"><span data-stu-id="be1c2-103">Creates an API Management Logger.</span></span>

## <span data-ttu-id="be1c2-104">句法</span><span class="sxs-lookup"><span data-stu-id="be1c2-104">SYNTAX</span></span>

### <span data-ttu-id="be1c2-105">EventHubLoggerSet (預設) </span><span class="sxs-lookup"><span data-stu-id="be1c2-105">EventHubLoggerSet (Default)</span></span>
```
New-AzApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be1c2-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="be1c2-106">ApplicationInsightsLoggerSet</span></span>
```
New-AzApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -InstrumentationKey <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be1c2-107">說明</span><span class="sxs-lookup"><span data-stu-id="be1c2-107">DESCRIPTION</span></span>
<span data-ttu-id="be1c2-108">**新的-AzApiManagementLogger** Cmdlet 會建立 Azure API 管理 **記錄器** 。</span><span class="sxs-lookup"><span data-stu-id="be1c2-108">The **New-AzApiManagementLogger** cmdlet creates an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="be1c2-109">示例</span><span class="sxs-lookup"><span data-stu-id="be1c2-109">EXAMPLES</span></span>

### <span data-ttu-id="be1c2-110">範例1：建立記錄器</span><span class="sxs-lookup"><span data-stu-id="be1c2-110">Example 1: Create a logger</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

<span data-ttu-id="be1c2-111">這個命令會使用指定的連接字串來建立名為 ContosoSdkEventHub 的記錄器。</span><span class="sxs-lookup"><span data-stu-id="be1c2-111">This command creates a logger named ContosoSdkEventHub by using the specified connection string.</span></span>

## <span data-ttu-id="be1c2-112">參數</span><span class="sxs-lookup"><span data-stu-id="be1c2-112">PARAMETERS</span></span>

### <span data-ttu-id="be1c2-113">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="be1c2-113">-ConnectionString</span></span>
<span data-ttu-id="be1c2-114">指定以下列開頭的 Azure 事件中心連接字串： `Endpoint=endpoint and key from Azure classic portal`</span><span class="sxs-lookup"><span data-stu-id="be1c2-114">Specifies an Azure Event Hubs connection string that starts with the following: `Endpoint=endpoint and key from Azure classic portal`</span></span>
<span data-ttu-id="be1c2-115">必須設定連接字串中具有傳送權利的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="be1c2-115">The Key with Send Rights in the connection string must be configured.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be1c2-116">-內容</span><span class="sxs-lookup"><span data-stu-id="be1c2-116">-Context</span></span>
<span data-ttu-id="be1c2-117">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="be1c2-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="be1c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be1c2-118">-DefaultProfile</span></span>
<span data-ttu-id="be1c2-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="be1c2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be1c2-120">-描述</span><span class="sxs-lookup"><span data-stu-id="be1c2-120">-Description</span></span>
<span data-ttu-id="be1c2-121">指定描述。</span><span class="sxs-lookup"><span data-stu-id="be1c2-121">Specifies a description.</span></span>

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

### <span data-ttu-id="be1c2-122">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="be1c2-122">-InstrumentationKey</span></span>
<span data-ttu-id="be1c2-123">Application Insights 的工具金鑰。</span><span class="sxs-lookup"><span data-stu-id="be1c2-123">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="be1c2-124">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="be1c2-124">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationInsightsLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be1c2-125">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="be1c2-125">-IsBuffered</span></span>
<span data-ttu-id="be1c2-126">指定是否要在發佈前緩衝記錄器中的記錄。</span><span class="sxs-lookup"><span data-stu-id="be1c2-126">Specifies whether the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="be1c2-127">預設值為 [$True]。</span><span class="sxs-lookup"><span data-stu-id="be1c2-127">The default value is $True.</span></span>
<span data-ttu-id="be1c2-128">當記錄經過緩衝處理時，會每隔15秒傳送給事件中心，或每當緩衝區收到 256 KB 的訊息。</span><span class="sxs-lookup"><span data-stu-id="be1c2-128">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be1c2-129">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="be1c2-129">-LoggerId</span></span>
<span data-ttu-id="be1c2-130">指定記錄器的 ID。</span><span class="sxs-lookup"><span data-stu-id="be1c2-130">Specifies an ID for the logger.</span></span>
<span data-ttu-id="be1c2-131">如果您沒有指定識別碼，此 Cmdlet 會產生一個 ID。</span><span class="sxs-lookup"><span data-stu-id="be1c2-131">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="be1c2-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="be1c2-132">-Name</span></span>
<span data-ttu-id="be1c2-133">從 Azure 傳統入口網站指定事件中心的機構名稱。</span><span class="sxs-lookup"><span data-stu-id="be1c2-133">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be1c2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be1c2-134">CommonParameters</span></span>
<span data-ttu-id="be1c2-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="be1c2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be1c2-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="be1c2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be1c2-137">輸入</span><span class="sxs-lookup"><span data-stu-id="be1c2-137">INPUTS</span></span>

### <span data-ttu-id="be1c2-138">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="be1c2-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="be1c2-139">System.object</span><span class="sxs-lookup"><span data-stu-id="be1c2-139">System.String</span></span>

### <span data-ttu-id="be1c2-140">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="be1c2-140">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="be1c2-141">輸出</span><span class="sxs-lookup"><span data-stu-id="be1c2-141">OUTPUTS</span></span>

### <span data-ttu-id="be1c2-142">ServiceManagement. PsApiManagementLogger （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="be1c2-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="be1c2-143">筆記</span><span class="sxs-lookup"><span data-stu-id="be1c2-143">NOTES</span></span>

## <span data-ttu-id="be1c2-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="be1c2-144">RELATED LINKS</span></span>

[<span data-ttu-id="be1c2-145">AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="be1c2-145">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="be1c2-146">移除-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="be1c2-146">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="be1c2-147">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="be1c2-147">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)

