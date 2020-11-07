---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 86438393-8D5A-46A0-B467-6A4434E18011
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42c8760dee1aa095086d4fad3309a3a5da64b296
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967755"
---
# <span data-ttu-id="5dbd4-101">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="5dbd4-101">Get-AzureService</span></span>

## <span data-ttu-id="5dbd4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5dbd4-102">SYNOPSIS</span></span>
<span data-ttu-id="5dbd4-103">傳回包含有關目前訂閱之雲端服務之資訊的物件。</span><span class="sxs-lookup"><span data-stu-id="5dbd4-103">Returns an object with information about the cloud services for the current subscription.</span></span>

## <span data-ttu-id="5dbd4-104">句法</span><span class="sxs-lookup"><span data-stu-id="5dbd4-104">SYNTAX</span></span>

```
Get-AzureService [[-ServiceName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5dbd4-105">說明</span><span class="sxs-lookup"><span data-stu-id="5dbd4-105">DESCRIPTION</span></span>
<span data-ttu-id="5dbd4-106">**AzureService** Cmdlet 會傳回與目前訂閱相關聯之所有 Azure 雲端服務的清單物件。</span><span class="sxs-lookup"><span data-stu-id="5dbd4-106">The **Get-AzureService** cmdlet returns a list object with all of the Azure cloud services associated with the current subscription.</span></span>
<span data-ttu-id="5dbd4-107">如果您指定 *ServiceName* 參數，則 **AzureService** 只會傳回相符服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5dbd4-107">If you specify the *ServiceName* parameter, **Get-AzureService** returns information on only the matching service.</span></span>

## <span data-ttu-id="5dbd4-108">示例</span><span class="sxs-lookup"><span data-stu-id="5dbd4-108">EXAMPLES</span></span>

### <span data-ttu-id="5dbd4-109">範例1：取得所有服務的相關資訊</span><span class="sxs-lookup"><span data-stu-id="5dbd4-109">Example 1: Get information about all services</span></span>
```
PS C:\> Get-AzureService
```

<span data-ttu-id="5dbd4-110">這個命令會傳回包含所有與目前訂閱相關的 Azure 服務資訊的物件。</span><span class="sxs-lookup"><span data-stu-id="5dbd4-110">This command returns an object that contains information about all of the Azure services associated with the current subscription.</span></span>

### <span data-ttu-id="5dbd4-111">範例2：取得指定服務的相關資訊</span><span class="sxs-lookup"><span data-stu-id="5dbd4-111">Example 2: Get information about a specified service</span></span>
```
PS C:\> Get-AzureService -ServiceName $MySvc
```

<span data-ttu-id="5dbd4-112">這個命令會傳回 $MySvc 服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5dbd4-112">This command returns information about the $MySvc service.</span></span>

### <span data-ttu-id="5dbd4-113">範例3：顯示可用的方法和屬性</span><span class="sxs-lookup"><span data-stu-id="5dbd4-113">Example 3: Display available methods and properties</span></span>
```
PS C:\> Get-AzureService | Get-Member
```

<span data-ttu-id="5dbd4-114">這個命令會顯示可從 **AzureService Cmdlet 取得** 的屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="5dbd4-114">This command displays the properties and methods that are available from the **Get-AzureService** cmdlet.</span></span>

## <span data-ttu-id="5dbd4-115">參數</span><span class="sxs-lookup"><span data-stu-id="5dbd4-115">PARAMETERS</span></span>

### <span data-ttu-id="5dbd4-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5dbd4-116">-InformationAction</span></span>
<span data-ttu-id="5dbd4-117">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="5dbd4-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5dbd4-118">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="5dbd4-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5dbd4-119">持續</span><span class="sxs-lookup"><span data-stu-id="5dbd4-119">Continue</span></span>
- <span data-ttu-id="5dbd4-120">理會</span><span class="sxs-lookup"><span data-stu-id="5dbd4-120">Ignore</span></span>
- <span data-ttu-id="5dbd4-121">看</span><span class="sxs-lookup"><span data-stu-id="5dbd4-121">Inquire</span></span>
- <span data-ttu-id="5dbd4-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5dbd4-122">SilentlyContinue</span></span>
- <span data-ttu-id="5dbd4-123">停止</span><span class="sxs-lookup"><span data-stu-id="5dbd4-123">Stop</span></span>
- <span data-ttu-id="5dbd4-124">封存</span><span class="sxs-lookup"><span data-stu-id="5dbd4-124">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dbd4-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5dbd4-125">-InformationVariable</span></span>
<span data-ttu-id="5dbd4-126">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="5dbd4-126">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dbd4-127">-設定檔</span><span class="sxs-lookup"><span data-stu-id="5dbd4-127">-Profile</span></span>
<span data-ttu-id="5dbd4-128">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="5dbd4-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5dbd4-129">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="5dbd4-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dbd4-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5dbd4-130">-ServiceName</span></span>
<span data-ttu-id="5dbd4-131">指定要傳回信息的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="5dbd4-131">Specifies the name of a service on which to return information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dbd4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dbd4-132">CommonParameters</span></span>
<span data-ttu-id="5dbd4-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5dbd4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dbd4-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5dbd4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dbd4-135">輸入</span><span class="sxs-lookup"><span data-stu-id="5dbd4-135">INPUTS</span></span>

## <span data-ttu-id="5dbd4-136">輸出</span><span class="sxs-lookup"><span data-stu-id="5dbd4-136">OUTPUTS</span></span>

### <span data-ttu-id="5dbd4-137">HostedServiceCoNtext</span><span class="sxs-lookup"><span data-stu-id="5dbd4-137">HostedServiceContext</span></span>

## <span data-ttu-id="5dbd4-138">筆記</span><span class="sxs-lookup"><span data-stu-id="5dbd4-138">NOTES</span></span>

## <span data-ttu-id="5dbd4-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="5dbd4-139">RELATED LINKS</span></span>

[<span data-ttu-id="5dbd4-140">新-AzureService</span><span class="sxs-lookup"><span data-stu-id="5dbd4-140">New-AzureService</span></span>](./New-AzureService.md)

[<span data-ttu-id="5dbd4-141">Set-AzureService</span><span class="sxs-lookup"><span data-stu-id="5dbd4-141">Set-AzureService</span></span>](./Set-AzureService.md)


