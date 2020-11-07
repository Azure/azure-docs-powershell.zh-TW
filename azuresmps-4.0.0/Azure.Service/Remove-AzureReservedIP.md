---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 761317FE-55FD-4DCC-B997-4F27D041470F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77f58c4f3ee1c440e35c43648f92d21793efddc2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967591"
---
# <span data-ttu-id="063ca-101">Remove-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="063ca-101">Remove-AzureReservedIP</span></span>

## <span data-ttu-id="063ca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="063ca-102">SYNOPSIS</span></span>
<span data-ttu-id="063ca-103">依名稱移除保留的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="063ca-103">Removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="063ca-104">句法</span><span class="sxs-lookup"><span data-stu-id="063ca-104">SYNTAX</span></span>

```
Remove-AzureReservedIP [-ReservedIPName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="063ca-105">說明</span><span class="sxs-lookup"><span data-stu-id="063ca-105">DESCRIPTION</span></span>
<span data-ttu-id="063ca-106">**AzureReservedIP** Cmdlet 會根據其名稱來移除保留的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="063ca-106">The **Remove-AzureReservedIP** cmdlet removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="063ca-107">示例</span><span class="sxs-lookup"><span data-stu-id="063ca-107">EXAMPLES</span></span>

### <span data-ttu-id="063ca-108">範例1：依名稱移除保留的 IP 位址</span><span class="sxs-lookup"><span data-stu-id="063ca-108">Example 1: Remove a reserved IP address by its name</span></span>
```
PS C:\> Remove-AzureReservedIP -ReservedIPName $name
```

<span data-ttu-id="063ca-109">這個命令會依名稱移除保留的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="063ca-109">This command removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="063ca-110">參數</span><span class="sxs-lookup"><span data-stu-id="063ca-110">PARAMETERS</span></span>

### <span data-ttu-id="063ca-111">-Force</span><span class="sxs-lookup"><span data-stu-id="063ca-111">-Force</span></span>
<span data-ttu-id="063ca-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="063ca-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="063ca-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="063ca-113">-InformationAction</span></span>
<span data-ttu-id="063ca-114">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="063ca-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="063ca-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="063ca-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="063ca-116">持續</span><span class="sxs-lookup"><span data-stu-id="063ca-116">Continue</span></span>
- <span data-ttu-id="063ca-117">理會</span><span class="sxs-lookup"><span data-stu-id="063ca-117">Ignore</span></span>
- <span data-ttu-id="063ca-118">看</span><span class="sxs-lookup"><span data-stu-id="063ca-118">Inquire</span></span>
- <span data-ttu-id="063ca-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="063ca-119">SilentlyContinue</span></span>
- <span data-ttu-id="063ca-120">停止</span><span class="sxs-lookup"><span data-stu-id="063ca-120">Stop</span></span>
- <span data-ttu-id="063ca-121">封存</span><span class="sxs-lookup"><span data-stu-id="063ca-121">Suspend</span></span>

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

### <span data-ttu-id="063ca-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="063ca-122">-InformationVariable</span></span>
<span data-ttu-id="063ca-123">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="063ca-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="063ca-124">-設定檔</span><span class="sxs-lookup"><span data-stu-id="063ca-124">-Profile</span></span>
<span data-ttu-id="063ca-125">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="063ca-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="063ca-126">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="063ca-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="063ca-127">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="063ca-127">-ReservedIPName</span></span>
<span data-ttu-id="063ca-128">指定保留 IP 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="063ca-128">Specifies the name of the reserved IP address.</span></span>

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

### <span data-ttu-id="063ca-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="063ca-129">CommonParameters</span></span>
<span data-ttu-id="063ca-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="063ca-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="063ca-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="063ca-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="063ca-132">輸入</span><span class="sxs-lookup"><span data-stu-id="063ca-132">INPUTS</span></span>

## <span data-ttu-id="063ca-133">輸出</span><span class="sxs-lookup"><span data-stu-id="063ca-133">OUTPUTS</span></span>

## <span data-ttu-id="063ca-134">筆記</span><span class="sxs-lookup"><span data-stu-id="063ca-134">NOTES</span></span>

## <span data-ttu-id="063ca-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="063ca-135">RELATED LINKS</span></span>

[<span data-ttu-id="063ca-136">AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="063ca-136">Get-AzureReservedIP</span></span>](./Get-AzureReservedIP.md)

[<span data-ttu-id="063ca-137">新-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="063ca-137">New-AzureReservedIP</span></span>](./New-AzureReservedIP.md)

[<span data-ttu-id="063ca-138">Set-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="063ca-138">Set-AzureReservedIPAssociation</span></span>](./Set-AzureReservedIPAssociation.md)


