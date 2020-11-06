---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
ms.openlocfilehash: 16a60f5f9951aaa40ac8da8584e1c2690206cdb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456276"
---
# <span data-ttu-id="cab68-101">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="cab68-101">Set-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="cab68-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cab68-102">SYNOPSIS</span></span>
<span data-ttu-id="cab68-103">修改 API 記錄管理器。</span><span class="sxs-lookup"><span data-stu-id="cab68-103">Modifies an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cab68-104">句法</span><span class="sxs-lookup"><span data-stu-id="cab68-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cab68-105">說明</span><span class="sxs-lookup"><span data-stu-id="cab68-105">DESCRIPTION</span></span>
<span data-ttu-id="cab68-106">**AzureRmApiManagementLogger** Cmdlet 會修改 Azure API 管理 **記錄** 程式的設定。</span><span class="sxs-lookup"><span data-stu-id="cab68-106">The **Set-AzureRmApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="cab68-107">示例</span><span class="sxs-lookup"><span data-stu-id="cab68-107">EXAMPLES</span></span>

### <span data-ttu-id="cab68-108">範例1：修改記錄器</span><span class="sxs-lookup"><span data-stu-id="cab68-108">Example 1: Modify a logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="cab68-109">這個命令會修改 ID 為 Logger123 的記錄器。</span><span class="sxs-lookup"><span data-stu-id="cab68-109">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="cab68-110">參數</span><span class="sxs-lookup"><span data-stu-id="cab68-110">PARAMETERS</span></span>

### <span data-ttu-id="cab68-111">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="cab68-111">-ConnectionString</span></span>
<span data-ttu-id="cab68-112">指定包含傳送原則許可權的 Azure 事件中心連線字串。</span><span class="sxs-lookup"><span data-stu-id="cab68-112">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cab68-113">-內容</span><span class="sxs-lookup"><span data-stu-id="cab68-113">-Context</span></span>
<span data-ttu-id="cab68-114">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="cab68-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cab68-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cab68-115">-DefaultProfile</span></span>
<span data-ttu-id="cab68-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cab68-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="cab68-117">-描述</span><span class="sxs-lookup"><span data-stu-id="cab68-117">-Description</span></span>
<span data-ttu-id="cab68-118">指定描述。</span><span class="sxs-lookup"><span data-stu-id="cab68-118">Specifies a description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cab68-119">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="cab68-119">-IsBuffered</span></span>
<span data-ttu-id="cab68-120">指定在發佈前先緩衝記錄器中的記錄。</span><span class="sxs-lookup"><span data-stu-id="cab68-120">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="cab68-121">當記錄經過緩衝處理時，會每隔15秒傳送給事件中心，或每當緩衝區收到 256 KB 的訊息。</span><span class="sxs-lookup"><span data-stu-id="cab68-121">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cab68-122">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="cab68-122">-LoggerId</span></span>
<span data-ttu-id="cab68-123">指定要更新的記錄器識別碼。</span><span class="sxs-lookup"><span data-stu-id="cab68-123">Specifies the ID of the logger to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cab68-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="cab68-124">-Name</span></span>
<span data-ttu-id="cab68-125">從 Azure 傳統入口網站指定事件中心的機構名稱。</span><span class="sxs-lookup"><span data-stu-id="cab68-125">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cab68-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cab68-126">-PassThru</span></span>
<span data-ttu-id="cab68-127">指示這個 Cmdlet 會傳回這個 Cmdlet 修改的  **PsApiManagementLogger** 。</span><span class="sxs-lookup"><span data-stu-id="cab68-127">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cab68-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cab68-128">CommonParameters</span></span>
<span data-ttu-id="cab68-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cab68-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cab68-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cab68-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cab68-131">輸入</span><span class="sxs-lookup"><span data-stu-id="cab68-131">INPUTS</span></span>

### <span data-ttu-id="cab68-132">所有</span><span class="sxs-lookup"><span data-stu-id="cab68-132">None</span></span>
<span data-ttu-id="cab68-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="cab68-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cab68-134">輸出</span><span class="sxs-lookup"><span data-stu-id="cab68-134">OUTPUTS</span></span>

### <span data-ttu-id="cab68-135">ServiceManagement. PsApiManagementLogger （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="cab68-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="cab68-136">筆記</span><span class="sxs-lookup"><span data-stu-id="cab68-136">NOTES</span></span>

## <span data-ttu-id="cab68-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="cab68-137">RELATED LINKS</span></span>

[<span data-ttu-id="cab68-138">AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="cab68-138">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="cab68-139">新-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="cab68-139">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="cab68-140">移除-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="cab68-140">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)


