---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CF429CF0-2AB2-4E31-8A0D-AE5C8D77A76B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0d1ad08d88cb5b89b0537b19f8ea4aaef0000cbb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967053"
---
# <span data-ttu-id="7c630-101">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="7c630-101">Get-AzureServiceADDomainExtension</span></span>

## <span data-ttu-id="7c630-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7c630-102">SYNOPSIS</span></span>
<span data-ttu-id="7c630-103">取得雲端服務 Active Directory (AD) 網域延伸適用于指定部署槽中的所有角色或命名角色。</span><span class="sxs-lookup"><span data-stu-id="7c630-103">Gets the cloud service Active Directory (AD) domain extension that applies to all roles or to named roles at a specified deployment slot.</span></span>

## <span data-ttu-id="7c630-104">句法</span><span class="sxs-lookup"><span data-stu-id="7c630-104">SYNTAX</span></span>

```
Get-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7c630-105">說明</span><span class="sxs-lookup"><span data-stu-id="7c630-105">DESCRIPTION</span></span>
<span data-ttu-id="7c630-106">**AzureServiceADDomainExtension** Cmdlet 會取得雲端服務 AD 網域延伸，該功能會套用至指定部署槽中的所有角色或命名角色。</span><span class="sxs-lookup"><span data-stu-id="7c630-106">The **Get-AzureServiceADDomainExtension** cmdlet gets the cloud service AD domain extension that applies to all roles or named roles at a specified deployment slot.</span></span>

## <span data-ttu-id="7c630-107">示例</span><span class="sxs-lookup"><span data-stu-id="7c630-107">EXAMPLES</span></span>

### <span data-ttu-id="7c630-108">範例1：取得指定服務的 AD 網域延伸</span><span class="sxs-lookup"><span data-stu-id="7c630-108">Example 1: Get the AD domain extension for a specified service</span></span>
```
PS C:\> Get-AzureServiceADDomainExtension -ServiceName $Svc
```

<span data-ttu-id="7c630-109">這個命令會取得 $Svc 中指定之服務的 AD 網域延伸。</span><span class="sxs-lookup"><span data-stu-id="7c630-109">This command gets the AD domain extension for the service specified in $Svc.</span></span>

## <span data-ttu-id="7c630-110">參數</span><span class="sxs-lookup"><span data-stu-id="7c630-110">PARAMETERS</span></span>

### <span data-ttu-id="7c630-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7c630-111">-InformationAction</span></span>
<span data-ttu-id="7c630-112">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="7c630-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7c630-113">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="7c630-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7c630-114">持續</span><span class="sxs-lookup"><span data-stu-id="7c630-114">Continue</span></span>
- <span data-ttu-id="7c630-115">理會</span><span class="sxs-lookup"><span data-stu-id="7c630-115">Ignore</span></span>
- <span data-ttu-id="7c630-116">看</span><span class="sxs-lookup"><span data-stu-id="7c630-116">Inquire</span></span>
- <span data-ttu-id="7c630-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7c630-117">SilentlyContinue</span></span>
- <span data-ttu-id="7c630-118">停止</span><span class="sxs-lookup"><span data-stu-id="7c630-118">Stop</span></span>
- <span data-ttu-id="7c630-119">封存</span><span class="sxs-lookup"><span data-stu-id="7c630-119">Suspend</span></span>

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

### <span data-ttu-id="7c630-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7c630-120">-InformationVariable</span></span>
<span data-ttu-id="7c630-121">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="7c630-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7c630-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="7c630-122">-Profile</span></span>
<span data-ttu-id="7c630-123">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="7c630-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7c630-124">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="7c630-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7c630-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7c630-125">-ServiceName</span></span>
<span data-ttu-id="7c630-126">指定部署的 Azure 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="7c630-126">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="7c630-127">-槽</span><span class="sxs-lookup"><span data-stu-id="7c630-127">-Slot</span></span>
<span data-ttu-id="7c630-128">指定部署環境。</span><span class="sxs-lookup"><span data-stu-id="7c630-128">Specifies the deployment environment.</span></span>
<span data-ttu-id="7c630-129">此參數可接受的值為： [生產] 或 [轉移]。</span><span class="sxs-lookup"><span data-stu-id="7c630-129">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="7c630-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c630-130">CommonParameters</span></span>
<span data-ttu-id="7c630-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7c630-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c630-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7c630-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c630-133">輸入</span><span class="sxs-lookup"><span data-stu-id="7c630-133">INPUTS</span></span>

## <span data-ttu-id="7c630-134">輸出</span><span class="sxs-lookup"><span data-stu-id="7c630-134">OUTPUTS</span></span>

## <span data-ttu-id="7c630-135">筆記</span><span class="sxs-lookup"><span data-stu-id="7c630-135">NOTES</span></span>

## <span data-ttu-id="7c630-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="7c630-136">RELATED LINKS</span></span>

[<span data-ttu-id="7c630-137">移除-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="7c630-137">Remove-AzureServiceADDomainExtension</span></span>](./Remove-AzureServiceADDomainExtension.md)

[<span data-ttu-id="7c630-138">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="7c630-138">Set-AzureServiceADDomainExtension</span></span>](./Set-AzureServiceADDomainExtension.md)


