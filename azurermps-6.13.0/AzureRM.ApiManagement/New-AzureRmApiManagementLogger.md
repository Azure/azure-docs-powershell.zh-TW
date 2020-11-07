---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
ms.openlocfilehash: 04119d70f1cf3ae01b1d74e24cb2e030eecaa46b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623441"
---
# <span data-ttu-id="c7d23-101">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c7d23-101">New-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="c7d23-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c7d23-102">SYNOPSIS</span></span>
<span data-ttu-id="c7d23-103">建立 API 記錄管理器。</span><span class="sxs-lookup"><span data-stu-id="c7d23-103">Creates an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7d23-104">句法</span><span class="sxs-lookup"><span data-stu-id="c7d23-104">SYNTAX</span></span>

### <span data-ttu-id="c7d23-105">EventHubLoggerSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c7d23-105">EventHubLoggerSet (Default)</span></span>
```
New-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7d23-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="c7d23-106">ApplicationInsightsLoggerSet</span></span>
```
New-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>]
 -InstrumentationKey <String> [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7d23-107">說明</span><span class="sxs-lookup"><span data-stu-id="c7d23-107">DESCRIPTION</span></span>
<span data-ttu-id="c7d23-108">**新的-AzureRmApiManagementLogger** Cmdlet 會建立 Azure API 管理 **記錄器** 。</span><span class="sxs-lookup"><span data-stu-id="c7d23-108">The **New-AzureRmApiManagementLogger** cmdlet creates an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="c7d23-109">示例</span><span class="sxs-lookup"><span data-stu-id="c7d23-109">EXAMPLES</span></span>

### <span data-ttu-id="c7d23-110">範例1：建立記錄器</span><span class="sxs-lookup"><span data-stu-id="c7d23-110">Example 1: Create a logger</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

<span data-ttu-id="c7d23-111">這個命令會使用指定的連接字串來建立名為 ContosoSdkEventHub 的記錄器。</span><span class="sxs-lookup"><span data-stu-id="c7d23-111">This command creates a logger named ContosoSdkEventHub by using the specified connection string.</span></span>

## <span data-ttu-id="c7d23-112">參數</span><span class="sxs-lookup"><span data-stu-id="c7d23-112">PARAMETERS</span></span>

### <span data-ttu-id="c7d23-113">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="c7d23-113">-ConnectionString</span></span>
<span data-ttu-id="c7d23-114">指定以下列開頭的 Azure 事件中心連接字串： `Endpoint=endpoint and key from Azure classic portal`</span><span class="sxs-lookup"><span data-stu-id="c7d23-114">Specifies an Azure Event Hubs connection string that starts with the following: `Endpoint=endpoint and key from Azure classic portal`</span></span>
<span data-ttu-id="c7d23-115">必須設定連接字串中具有傳送權利的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="c7d23-115">The Key with Send Rights in the connection string must be configured.</span></span>

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

### <span data-ttu-id="c7d23-116">-內容</span><span class="sxs-lookup"><span data-stu-id="c7d23-116">-Context</span></span>
<span data-ttu-id="c7d23-117">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="c7d23-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c7d23-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7d23-118">-DefaultProfile</span></span>
<span data-ttu-id="c7d23-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c7d23-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7d23-120">-描述</span><span class="sxs-lookup"><span data-stu-id="c7d23-120">-Description</span></span>
<span data-ttu-id="c7d23-121">指定描述。</span><span class="sxs-lookup"><span data-stu-id="c7d23-121">Specifies a description.</span></span>

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

### <span data-ttu-id="c7d23-122">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="c7d23-122">-InstrumentationKey</span></span>
<span data-ttu-id="c7d23-123">Application Insights 的工具金鑰。</span><span class="sxs-lookup"><span data-stu-id="c7d23-123">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="c7d23-124">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="c7d23-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="c7d23-125">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="c7d23-125">-IsBuffered</span></span>
<span data-ttu-id="c7d23-126">指定是否要在發佈前緩衝記錄器中的記錄。</span><span class="sxs-lookup"><span data-stu-id="c7d23-126">Specifies whether the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="c7d23-127">預設值為 [$True]。</span><span class="sxs-lookup"><span data-stu-id="c7d23-127">The default value is $True.</span></span>
<span data-ttu-id="c7d23-128">當記錄經過緩衝處理時，會每隔15秒傳送給事件中心，或每當緩衝區收到 256 KB 的訊息。</span><span class="sxs-lookup"><span data-stu-id="c7d23-128">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

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

### <span data-ttu-id="c7d23-129">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="c7d23-129">-LoggerId</span></span>
<span data-ttu-id="c7d23-130">指定記錄器的 ID。</span><span class="sxs-lookup"><span data-stu-id="c7d23-130">Specifies an ID for the logger.</span></span>
<span data-ttu-id="c7d23-131">如果您沒有指定識別碼，此 Cmdlet 會產生一個 ID。</span><span class="sxs-lookup"><span data-stu-id="c7d23-131">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="c7d23-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="c7d23-132">-Name</span></span>
<span data-ttu-id="c7d23-133">從 Azure 傳統入口網站指定事件中心的機構名稱。</span><span class="sxs-lookup"><span data-stu-id="c7d23-133">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="c7d23-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7d23-134">CommonParameters</span></span>
<span data-ttu-id="c7d23-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c7d23-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7d23-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c7d23-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7d23-137">輸入</span><span class="sxs-lookup"><span data-stu-id="c7d23-137">INPUTS</span></span>

### <span data-ttu-id="c7d23-138">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="c7d23-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c7d23-139">System.object</span><span class="sxs-lookup"><span data-stu-id="c7d23-139">System.String</span></span>

### <span data-ttu-id="c7d23-140">系統為 Nullable "1 [[System.object，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c7d23-140">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="c7d23-141">輸出</span><span class="sxs-lookup"><span data-stu-id="c7d23-141">OUTPUTS</span></span>

### <span data-ttu-id="c7d23-142">ServiceManagement. PsApiManagementLogger （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="c7d23-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="c7d23-143">筆記</span><span class="sxs-lookup"><span data-stu-id="c7d23-143">NOTES</span></span>

## <span data-ttu-id="c7d23-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="c7d23-144">RELATED LINKS</span></span>

[<span data-ttu-id="c7d23-145">AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c7d23-145">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="c7d23-146">移除-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c7d23-146">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="c7d23-147">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c7d23-147">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


