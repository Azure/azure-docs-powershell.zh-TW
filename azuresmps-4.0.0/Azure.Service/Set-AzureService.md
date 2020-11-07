---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4A920D84-0005-45A2-8229-FD9436A2CA6D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 927520466299776326229976b355444f9db6c23e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967495"
---
# <span data-ttu-id="98536-101">Set-AzureService</span><span class="sxs-lookup"><span data-stu-id="98536-101">Set-AzureService</span></span>

## <span data-ttu-id="98536-102">摘要</span><span class="sxs-lookup"><span data-stu-id="98536-102">SYNOPSIS</span></span>
<span data-ttu-id="98536-103">設定或更新指定 Microsoft Azure 服務的標籤及描述。</span><span class="sxs-lookup"><span data-stu-id="98536-103">Sets or updates the label and description of the specified Microsoft Azure service.</span></span>

## <span data-ttu-id="98536-104">句法</span><span class="sxs-lookup"><span data-stu-id="98536-104">SYNTAX</span></span>

```
Set-AzureService [-ServiceName] <String> [[-Label] <String>] [[-Description] <String>]
 [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="98536-105">說明</span><span class="sxs-lookup"><span data-stu-id="98536-105">DESCRIPTION</span></span>
<span data-ttu-id="98536-106">**AzureService** Cmdlet 會將標籤和描述指派給目前訂閱中的服務。</span><span class="sxs-lookup"><span data-stu-id="98536-106">The **Set-AzureService** cmdlet assigns a label and description to a service in the current subscription.</span></span>

## <span data-ttu-id="98536-107">示例</span><span class="sxs-lookup"><span data-stu-id="98536-107">EXAMPLES</span></span>

### <span data-ttu-id="98536-108">範例1：更新服務的標籤和描述</span><span class="sxs-lookup"><span data-stu-id="98536-108">Example 1: Update the label and description for a service</span></span>
```
PS C:\> C:\PS>Set-AzureService -ServiceName "MySvc1" -Label "MyTestSvc1" -Description "My service for testing out new configurations"
```

<span data-ttu-id="98536-109">這個命令會將標籤設為 "MyTestSvc1"，並將描述設定為 [我的服務用來測試新的配置]，以供 MyTestSvc1 服務。</span><span class="sxs-lookup"><span data-stu-id="98536-109">This command sets the label to "MyTestSvc1" and the description to "My service for testing out new configurations" for the MyTestSvc1 service.</span></span>

## <span data-ttu-id="98536-110">參數</span><span class="sxs-lookup"><span data-stu-id="98536-110">PARAMETERS</span></span>

### <span data-ttu-id="98536-111">-描述</span><span class="sxs-lookup"><span data-stu-id="98536-111">-Description</span></span>
<span data-ttu-id="98536-112">指定 Azure 服務的描述。</span><span class="sxs-lookup"><span data-stu-id="98536-112">Specifies a description for the Azure service.</span></span>
<span data-ttu-id="98536-113">描述最多可以為1024個字元。</span><span class="sxs-lookup"><span data-stu-id="98536-113">The description may be up to 1024 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98536-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="98536-114">-InformationAction</span></span>
<span data-ttu-id="98536-115">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="98536-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="98536-116">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="98536-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="98536-117">持續</span><span class="sxs-lookup"><span data-stu-id="98536-117">Continue</span></span>
- <span data-ttu-id="98536-118">理會</span><span class="sxs-lookup"><span data-stu-id="98536-118">Ignore</span></span>
- <span data-ttu-id="98536-119">看</span><span class="sxs-lookup"><span data-stu-id="98536-119">Inquire</span></span>
- <span data-ttu-id="98536-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="98536-120">SilentlyContinue</span></span>
- <span data-ttu-id="98536-121">停止</span><span class="sxs-lookup"><span data-stu-id="98536-121">Stop</span></span>
- <span data-ttu-id="98536-122">封存</span><span class="sxs-lookup"><span data-stu-id="98536-122">Suspend</span></span>

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

### <span data-ttu-id="98536-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="98536-123">-InformationVariable</span></span>
<span data-ttu-id="98536-124">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="98536-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="98536-125">-標籤</span><span class="sxs-lookup"><span data-stu-id="98536-125">-Label</span></span>
<span data-ttu-id="98536-126">指定 Azure 服務的標籤。</span><span class="sxs-lookup"><span data-stu-id="98536-126">Specifies a label for the Azure service.</span></span>
<span data-ttu-id="98536-127">標籤長度最多可為100個字元。</span><span class="sxs-lookup"><span data-stu-id="98536-127">The label may be up to 100 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98536-128">-設定檔</span><span class="sxs-lookup"><span data-stu-id="98536-128">-Profile</span></span>
<span data-ttu-id="98536-129">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="98536-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="98536-130">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="98536-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="98536-131">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="98536-131">-ReverseDnsFqdn</span></span>
<span data-ttu-id="98536-132">指定反向 DNS 的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="98536-132">Specifies the fully qualified domain name for reverse DNS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98536-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="98536-133">-ServiceName</span></span>
<span data-ttu-id="98536-134">指定要更新的 Azure 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="98536-134">Specifies the name of the Azure service to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98536-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98536-135">CommonParameters</span></span>
<span data-ttu-id="98536-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="98536-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98536-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="98536-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98536-138">輸入</span><span class="sxs-lookup"><span data-stu-id="98536-138">INPUTS</span></span>

## <span data-ttu-id="98536-139">輸出</span><span class="sxs-lookup"><span data-stu-id="98536-139">OUTPUTS</span></span>

### <span data-ttu-id="98536-140">ManagementOperationCoNtext</span><span class="sxs-lookup"><span data-stu-id="98536-140">ManagementOperationContext</span></span>

## <span data-ttu-id="98536-141">筆記</span><span class="sxs-lookup"><span data-stu-id="98536-141">NOTES</span></span>

## <span data-ttu-id="98536-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="98536-142">RELATED LINKS</span></span>

[<span data-ttu-id="98536-143">AzureService</span><span class="sxs-lookup"><span data-stu-id="98536-143">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="98536-144">新-AzureService</span><span class="sxs-lookup"><span data-stu-id="98536-144">New-AzureService</span></span>](./New-AzureService.md)


