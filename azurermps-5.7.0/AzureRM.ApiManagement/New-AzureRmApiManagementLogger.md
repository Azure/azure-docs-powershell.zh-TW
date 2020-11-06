---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
ms.openlocfilehash: 2929cbd89328d971b47b748d4aa042ade13c1af9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448786"
---
# <span data-ttu-id="b6437-101">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="b6437-101">New-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="b6437-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b6437-102">SYNOPSIS</span></span>
<span data-ttu-id="b6437-103">建立 API 記錄管理器。</span><span class="sxs-lookup"><span data-stu-id="b6437-103">Creates an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6437-104">句法</span><span class="sxs-lookup"><span data-stu-id="b6437-104">SYNTAX</span></span>

```
New-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6437-105">說明</span><span class="sxs-lookup"><span data-stu-id="b6437-105">DESCRIPTION</span></span>
<span data-ttu-id="b6437-106">**新的-AzureRmApiManagementLogger** Cmdlet 會建立 Azure API 管理 **記錄器** 。</span><span class="sxs-lookup"><span data-stu-id="b6437-106">The **New-AzureRmApiManagementLogger** cmdlet creates an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="b6437-107">示例</span><span class="sxs-lookup"><span data-stu-id="b6437-107">EXAMPLES</span></span>

### <span data-ttu-id="b6437-108">範例1：建立記錄器</span><span class="sxs-lookup"><span data-stu-id="b6437-108">Example 1: Create a logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

<span data-ttu-id="b6437-109">這個命令會使用指定的連接字串來建立名為 ContosoSdkEventHub 的記錄器。</span><span class="sxs-lookup"><span data-stu-id="b6437-109">This command creates a logger named ContosoSdkEventHub by using the specified connection string.</span></span>

## <span data-ttu-id="b6437-110">參數</span><span class="sxs-lookup"><span data-stu-id="b6437-110">PARAMETERS</span></span>

### <span data-ttu-id="b6437-111">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="b6437-111">-ConnectionString</span></span>
<span data-ttu-id="b6437-112">指定以下列開頭的 Azure 事件中心連接字串：</span><span class="sxs-lookup"><span data-stu-id="b6437-112">Specifies an Azure Event Hubs connection string that starts with the following:</span></span> 

`Endpoint=endpoint and key from Azure classic portal`

<span data-ttu-id="b6437-113">必須設定連接字串中具有傳送權利的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="b6437-113">The Key with Send Rights in the connection string must be configured.</span></span>

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

### <span data-ttu-id="b6437-114">-內容</span><span class="sxs-lookup"><span data-stu-id="b6437-114">-Context</span></span>
<span data-ttu-id="b6437-115">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="b6437-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b6437-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6437-116">-DefaultProfile</span></span>
<span data-ttu-id="b6437-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b6437-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="b6437-118">-描述</span><span class="sxs-lookup"><span data-stu-id="b6437-118">-Description</span></span>
<span data-ttu-id="b6437-119">指定描述。</span><span class="sxs-lookup"><span data-stu-id="b6437-119">Specifies a description.</span></span>

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

### <span data-ttu-id="b6437-120">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="b6437-120">-IsBuffered</span></span>
<span data-ttu-id="b6437-121">指定是否要在發佈前緩衝記錄器中的記錄。</span><span class="sxs-lookup"><span data-stu-id="b6437-121">Specifies whether the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="b6437-122">預設值為 [$True]。</span><span class="sxs-lookup"><span data-stu-id="b6437-122">The default value is $True.</span></span>
<span data-ttu-id="b6437-123">當記錄經過緩衝處理時，會每隔15秒傳送給事件中心，或每當緩衝區收到 256 KB 的訊息。</span><span class="sxs-lookup"><span data-stu-id="b6437-123">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6437-124">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="b6437-124">-LoggerId</span></span>
<span data-ttu-id="b6437-125">指定記錄器的 ID。</span><span class="sxs-lookup"><span data-stu-id="b6437-125">Specifies an ID for the logger.</span></span>
<span data-ttu-id="b6437-126">如果您沒有指定識別碼，此 Cmdlet 會產生一個 ID。</span><span class="sxs-lookup"><span data-stu-id="b6437-126">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="b6437-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="b6437-127">-Name</span></span>
<span data-ttu-id="b6437-128">從 Azure 傳統入口網站指定事件中心的機構名稱。</span><span class="sxs-lookup"><span data-stu-id="b6437-128">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="b6437-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6437-129">CommonParameters</span></span>
<span data-ttu-id="b6437-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b6437-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6437-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b6437-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6437-132">輸入</span><span class="sxs-lookup"><span data-stu-id="b6437-132">INPUTS</span></span>

### <span data-ttu-id="b6437-133">所有</span><span class="sxs-lookup"><span data-stu-id="b6437-133">None</span></span>
<span data-ttu-id="b6437-134">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="b6437-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b6437-135">輸出</span><span class="sxs-lookup"><span data-stu-id="b6437-135">OUTPUTS</span></span>

### <span data-ttu-id="b6437-136">ServiceManagement. PsApiManagementLogger （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="b6437-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="b6437-137">筆記</span><span class="sxs-lookup"><span data-stu-id="b6437-137">NOTES</span></span>

## <span data-ttu-id="b6437-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6437-138">RELATED LINKS</span></span>

[<span data-ttu-id="b6437-139">AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="b6437-139">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="b6437-140">移除-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="b6437-140">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="b6437-141">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="b6437-141">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


