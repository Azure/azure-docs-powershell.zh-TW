---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
ms.openlocfilehash: c21c227dd748f28523f4ac616d003e029d19e38f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450928"
---
# <span data-ttu-id="36d43-101">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="36d43-101">Set-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="36d43-102">摘要</span><span class="sxs-lookup"><span data-stu-id="36d43-102">SYNOPSIS</span></span>
<span data-ttu-id="36d43-103">修改 API 記錄管理器。</span><span class="sxs-lookup"><span data-stu-id="36d43-103">Modifies an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36d43-104">句法</span><span class="sxs-lookup"><span data-stu-id="36d43-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36d43-105">說明</span><span class="sxs-lookup"><span data-stu-id="36d43-105">DESCRIPTION</span></span>
<span data-ttu-id="36d43-106">**AzureRmApiManagementLogger** Cmdlet 會修改 Azure API 管理 **記錄** 程式的設定。</span><span class="sxs-lookup"><span data-stu-id="36d43-106">The **Set-AzureRmApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="36d43-107">示例</span><span class="sxs-lookup"><span data-stu-id="36d43-107">EXAMPLES</span></span>

### <span data-ttu-id="36d43-108">範例1：修改記錄器</span><span class="sxs-lookup"><span data-stu-id="36d43-108">Example 1: Modify a logger</span></span>
```
PS C:\>Set-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="36d43-109">這個命令會修改 ID 為 Logger123 的記錄器。</span><span class="sxs-lookup"><span data-stu-id="36d43-109">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="36d43-110">參數</span><span class="sxs-lookup"><span data-stu-id="36d43-110">PARAMETERS</span></span>

### <span data-ttu-id="36d43-111">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="36d43-111">-ConnectionString</span></span>
<span data-ttu-id="36d43-112">指定包含傳送原則許可權的 Azure 事件中心連線字串。</span><span class="sxs-lookup"><span data-stu-id="36d43-112">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

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

### <span data-ttu-id="36d43-113">-內容</span><span class="sxs-lookup"><span data-stu-id="36d43-113">-Context</span></span>
<span data-ttu-id="36d43-114">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="36d43-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="36d43-115">-描述</span><span class="sxs-lookup"><span data-stu-id="36d43-115">-Description</span></span>
<span data-ttu-id="36d43-116">指定描述。</span><span class="sxs-lookup"><span data-stu-id="36d43-116">Specifies a description.</span></span>

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

### <span data-ttu-id="36d43-117">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="36d43-117">-IsBuffered</span></span>
<span data-ttu-id="36d43-118">指定在發佈前先緩衝記錄器中的記錄。</span><span class="sxs-lookup"><span data-stu-id="36d43-118">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="36d43-119">當記錄經過緩衝處理時，會每隔15秒傳送給事件中心，或每當緩衝區收到 256 KB 的訊息。</span><span class="sxs-lookup"><span data-stu-id="36d43-119">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

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

### <span data-ttu-id="36d43-120">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="36d43-120">-LoggerId</span></span>
<span data-ttu-id="36d43-121">指定要更新的記錄器識別碼。</span><span class="sxs-lookup"><span data-stu-id="36d43-121">Specifies the ID of the logger to update.</span></span>

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

### <span data-ttu-id="36d43-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="36d43-122">-Name</span></span>
<span data-ttu-id="36d43-123">從 Azure 傳統入口網站指定事件中心的機構名稱。</span><span class="sxs-lookup"><span data-stu-id="36d43-123">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="36d43-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36d43-124">-PassThru</span></span>
<span data-ttu-id="36d43-125">指示這個 Cmdlet 會傳回這個 Cmdlet 修改的  **PsApiManagementLogger** 。</span><span class="sxs-lookup"><span data-stu-id="36d43-125">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="36d43-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36d43-126">-DefaultProfile</span></span>
<span data-ttu-id="36d43-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="36d43-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36d43-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36d43-128">CommonParameters</span></span>
<span data-ttu-id="36d43-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="36d43-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36d43-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="36d43-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36d43-131">輸入</span><span class="sxs-lookup"><span data-stu-id="36d43-131">INPUTS</span></span>

## <span data-ttu-id="36d43-132">輸出</span><span class="sxs-lookup"><span data-stu-id="36d43-132">OUTPUTS</span></span>

### <span data-ttu-id="36d43-133">ServiceManagement. PsApiManagementLogger （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="36d43-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="36d43-134">筆記</span><span class="sxs-lookup"><span data-stu-id="36d43-134">NOTES</span></span>

## <span data-ttu-id="36d43-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="36d43-135">RELATED LINKS</span></span>

[<span data-ttu-id="36d43-136">AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="36d43-136">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="36d43-137">新-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="36d43-137">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="36d43-138">移除-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="36d43-138">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)


