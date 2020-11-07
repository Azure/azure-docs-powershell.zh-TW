---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C0EEC51F-F8AB-4A6C-8F99-2B2DFFE9BB26
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9b5f4d5319e705c4f0481edcb5a44a579f4ff01d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967064"
---
# <span data-ttu-id="8cbb7-101">Get-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="8cbb7-101">Get-AzureReservedIP</span></span>

## <span data-ttu-id="8cbb7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8cbb7-102">SYNOPSIS</span></span>
<span data-ttu-id="8cbb7-103">根據其名稱取得保留的 IP 位址，或列出訂閱中所有保留的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="8cbb7-103">Gets a reserved IP address by its name or lists all the reserved IP addresses in the subscription.</span></span>

## <span data-ttu-id="8cbb7-104">句法</span><span class="sxs-lookup"><span data-stu-id="8cbb7-104">SYNTAX</span></span>

```
Get-AzureReservedIP [[-ReservedIPName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8cbb7-105">說明</span><span class="sxs-lookup"><span data-stu-id="8cbb7-105">DESCRIPTION</span></span>
<span data-ttu-id="8cbb7-106">**AzureReservedIP** Cmdlet 會根據其名稱取得保留的 ip 位址，或列出訂閱中所有保留的 ip 位址。</span><span class="sxs-lookup"><span data-stu-id="8cbb7-106">The **Get-AzureReservedIP** cmdlet gets a reserved IP address by its name or lists all of the reserved IP addresses in the subscription.</span></span>

## <span data-ttu-id="8cbb7-107">示例</span><span class="sxs-lookup"><span data-stu-id="8cbb7-107">EXAMPLES</span></span>

### <span data-ttu-id="8cbb7-108">範例1：取得所有保留 IP 位址</span><span class="sxs-lookup"><span data-stu-id="8cbb7-108">Example 1: Get all reserved IP addresses</span></span>
```
PS C:\> Get-AzureReservedIP
```

<span data-ttu-id="8cbb7-109">這個命令會取得所有保留的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="8cbb7-109">This command gets all reserved IP addresses.</span></span>

### <span data-ttu-id="8cbb7-110">範例2：取得指定名稱的保留 IP 位址</span><span class="sxs-lookup"><span data-stu-id="8cbb7-110">Example 2: Get a reserved IP address with a specified name</span></span>
```
PS C:\> Get-AzureReservedIP -ReservedIPName $IpName
```

<span data-ttu-id="8cbb7-111">這個命令會取得具有 $IpName 變數所指定之名稱的保留 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="8cbb7-111">This command gets the reserved IP address that has the name specified by the $IpName variable.</span></span>

## <span data-ttu-id="8cbb7-112">參數</span><span class="sxs-lookup"><span data-stu-id="8cbb7-112">PARAMETERS</span></span>

### <span data-ttu-id="8cbb7-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8cbb7-113">-InformationAction</span></span>
<span data-ttu-id="8cbb7-114">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="8cbb7-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8cbb7-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="8cbb7-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8cbb7-116">持續</span><span class="sxs-lookup"><span data-stu-id="8cbb7-116">Continue</span></span>
- <span data-ttu-id="8cbb7-117">理會</span><span class="sxs-lookup"><span data-stu-id="8cbb7-117">Ignore</span></span>
- <span data-ttu-id="8cbb7-118">看</span><span class="sxs-lookup"><span data-stu-id="8cbb7-118">Inquire</span></span>
- <span data-ttu-id="8cbb7-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8cbb7-119">SilentlyContinue</span></span>
- <span data-ttu-id="8cbb7-120">停止</span><span class="sxs-lookup"><span data-stu-id="8cbb7-120">Stop</span></span>
- <span data-ttu-id="8cbb7-121">封存</span><span class="sxs-lookup"><span data-stu-id="8cbb7-121">Suspend</span></span>

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

### <span data-ttu-id="8cbb7-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8cbb7-122">-InformationVariable</span></span>
<span data-ttu-id="8cbb7-123">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="8cbb7-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8cbb7-124">-設定檔</span><span class="sxs-lookup"><span data-stu-id="8cbb7-124">-Profile</span></span>
<span data-ttu-id="8cbb7-125">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="8cbb7-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8cbb7-126">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="8cbb7-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8cbb7-127">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="8cbb7-127">-ReservedIPName</span></span>
<span data-ttu-id="8cbb7-128">指定保留的 IP 名稱。</span><span class="sxs-lookup"><span data-stu-id="8cbb7-128">Specifies the reserved IP name.</span></span>

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

### <span data-ttu-id="8cbb7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cbb7-129">CommonParameters</span></span>
<span data-ttu-id="8cbb7-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8cbb7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cbb7-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8cbb7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cbb7-132">輸入</span><span class="sxs-lookup"><span data-stu-id="8cbb7-132">INPUTS</span></span>

## <span data-ttu-id="8cbb7-133">輸出</span><span class="sxs-lookup"><span data-stu-id="8cbb7-133">OUTPUTS</span></span>

## <span data-ttu-id="8cbb7-134">筆記</span><span class="sxs-lookup"><span data-stu-id="8cbb7-134">NOTES</span></span>

## <span data-ttu-id="8cbb7-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="8cbb7-135">RELATED LINKS</span></span>

[<span data-ttu-id="8cbb7-136">新-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="8cbb7-136">New-AzureReservedIP</span></span>](./New-AzureReservedIP.md)

[<span data-ttu-id="8cbb7-137">移除-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="8cbb7-137">Remove-AzureReservedIP</span></span>](./Remove-AzureReservedIP.md)


