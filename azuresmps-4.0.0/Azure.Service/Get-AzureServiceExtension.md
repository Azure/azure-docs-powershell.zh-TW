---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2664607C-FF95-4EB7-869E-A421343B0517
online version: ''
schema: 2.0.0
ms.openlocfilehash: 231f24a20471d8a4639b091c10d0e04f65b71b76
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967045"
---
# <span data-ttu-id="81dd7-101">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="81dd7-101">Get-AzureServiceExtension</span></span>

## <span data-ttu-id="81dd7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81dd7-102">SYNOPSIS</span></span>
<span data-ttu-id="81dd7-103">取得在部署中套用的雲端服務擴充。</span><span class="sxs-lookup"><span data-stu-id="81dd7-103">Gets cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="81dd7-104">句法</span><span class="sxs-lookup"><span data-stu-id="81dd7-104">SYNTAX</span></span>

```
Get-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-ExtensionName] <String>]
 [[-ProviderNamespace] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="81dd7-105">說明</span><span class="sxs-lookup"><span data-stu-id="81dd7-105">DESCRIPTION</span></span>
<span data-ttu-id="81dd7-106">**AzureServiceExtension** Cmdlet 會取得在部署中套用的現有雲端服務延伸。</span><span class="sxs-lookup"><span data-stu-id="81dd7-106">The **Get-AzureServiceExtension** cmdlet gets existing cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="81dd7-107">示例</span><span class="sxs-lookup"><span data-stu-id="81dd7-107">EXAMPLES</span></span>

### <span data-ttu-id="81dd7-108">範例1：取得指定的延伸</span><span class="sxs-lookup"><span data-stu-id="81dd7-108">Example 1: Get a specified extension</span></span>
```
PS C:\> Get-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions"
```

<span data-ttu-id="81dd7-109">這個命令會以指定的名稱和命名空間來取得雲端服務延伸。</span><span class="sxs-lookup"><span data-stu-id="81dd7-109">This command gets the cloud service extension with the specified name and namespace.</span></span>

## <span data-ttu-id="81dd7-110">參數</span><span class="sxs-lookup"><span data-stu-id="81dd7-110">PARAMETERS</span></span>

### <span data-ttu-id="81dd7-111">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="81dd7-111">-ExtensionName</span></span>
<span data-ttu-id="81dd7-112">指定副檔名。</span><span class="sxs-lookup"><span data-stu-id="81dd7-112">Specifies the extension name.</span></span>

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

### <span data-ttu-id="81dd7-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="81dd7-113">-InformationAction</span></span>
<span data-ttu-id="81dd7-114">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="81dd7-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="81dd7-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="81dd7-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="81dd7-116">持續</span><span class="sxs-lookup"><span data-stu-id="81dd7-116">Continue</span></span>
- <span data-ttu-id="81dd7-117">理會</span><span class="sxs-lookup"><span data-stu-id="81dd7-117">Ignore</span></span>
- <span data-ttu-id="81dd7-118">看</span><span class="sxs-lookup"><span data-stu-id="81dd7-118">Inquire</span></span>
- <span data-ttu-id="81dd7-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="81dd7-119">SilentlyContinue</span></span>
- <span data-ttu-id="81dd7-120">停止</span><span class="sxs-lookup"><span data-stu-id="81dd7-120">Stop</span></span>
- <span data-ttu-id="81dd7-121">封存</span><span class="sxs-lookup"><span data-stu-id="81dd7-121">Suspend</span></span>

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

### <span data-ttu-id="81dd7-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="81dd7-122">-InformationVariable</span></span>
<span data-ttu-id="81dd7-123">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="81dd7-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="81dd7-124">-設定檔</span><span class="sxs-lookup"><span data-stu-id="81dd7-124">-Profile</span></span>
<span data-ttu-id="81dd7-125">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="81dd7-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="81dd7-126">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="81dd7-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="81dd7-127">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="81dd7-127">-ProviderNamespace</span></span>
<span data-ttu-id="81dd7-128">指定延伸提供者命名空間。</span><span class="sxs-lookup"><span data-stu-id="81dd7-128">Specifies the extension provider namespace.</span></span>

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

### <span data-ttu-id="81dd7-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="81dd7-129">-ServiceName</span></span>
<span data-ttu-id="81dd7-130">指定部署的 Azure 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="81dd7-130">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="81dd7-131">-槽</span><span class="sxs-lookup"><span data-stu-id="81dd7-131">-Slot</span></span>
<span data-ttu-id="81dd7-132">指定部署環境。</span><span class="sxs-lookup"><span data-stu-id="81dd7-132">Specifies the deployment environment.</span></span>
<span data-ttu-id="81dd7-133">此參數可接受的值為： [生產] 或 [轉移]。</span><span class="sxs-lookup"><span data-stu-id="81dd7-133">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="81dd7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81dd7-134">CommonParameters</span></span>
<span data-ttu-id="81dd7-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81dd7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81dd7-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="81dd7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81dd7-137">輸入</span><span class="sxs-lookup"><span data-stu-id="81dd7-137">INPUTS</span></span>

## <span data-ttu-id="81dd7-138">輸出</span><span class="sxs-lookup"><span data-stu-id="81dd7-138">OUTPUTS</span></span>

## <span data-ttu-id="81dd7-139">筆記</span><span class="sxs-lookup"><span data-stu-id="81dd7-139">NOTES</span></span>

## <span data-ttu-id="81dd7-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="81dd7-140">RELATED LINKS</span></span>

[<span data-ttu-id="81dd7-141">移除-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="81dd7-141">Remove-AzureServiceExtension</span></span>](./Remove-AzureServiceExtension.md)

[<span data-ttu-id="81dd7-142">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="81dd7-142">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)


