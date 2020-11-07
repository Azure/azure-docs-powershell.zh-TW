---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1085388B-0855-4E29-9043-3FE2C638F58D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22c97045cb5f85256ec4d252cdbfb13c59643008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967370"
---
# <span data-ttu-id="3dd04-101">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="3dd04-101">New-AzureDns</span></span>

## <span data-ttu-id="3dd04-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3dd04-102">SYNOPSIS</span></span>
<span data-ttu-id="3dd04-103">建立 Azure DNS settings 物件。</span><span class="sxs-lookup"><span data-stu-id="3dd04-103">Creates an Azure DNS settings object.</span></span>

## <span data-ttu-id="3dd04-104">句法</span><span class="sxs-lookup"><span data-stu-id="3dd04-104">SYNTAX</span></span>

```
New-AzureDns [-Name] <String> [-IPAddress] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3dd04-105">說明</span><span class="sxs-lookup"><span data-stu-id="3dd04-105">DESCRIPTION</span></span>
<span data-ttu-id="3dd04-106">**新的-AzureDns** Cmdlet 會建立 Azure DNS settings 物件。</span><span class="sxs-lookup"><span data-stu-id="3dd04-106">The **New-AzureDns** cmdlet creates an Azure DNS settings object.</span></span>
<span data-ttu-id="3dd04-107">當您使用 **新的 add-azurevm** Cmdlet 建立虛擬機器時，您可以使用 DNS 設定物件。</span><span class="sxs-lookup"><span data-stu-id="3dd04-107">You can use a DNS settings object when you create a virtual machine by using the **New-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="3dd04-108">示例</span><span class="sxs-lookup"><span data-stu-id="3dd04-108">EXAMPLES</span></span>

### <span data-ttu-id="3dd04-109">範例1：建立 DNS 設定物件</span><span class="sxs-lookup"><span data-stu-id="3dd04-109">Example 1: Create a DNS settings object</span></span>
```
PS C:\> $Dns = New-AzureDns -Name "Dns01" -IPAddress "10.1.2.4"
```

<span data-ttu-id="3dd04-110">這個命令會建立 Azure DNS 設定物件。</span><span class="sxs-lookup"><span data-stu-id="3dd04-110">This command creates an Azure DNS settings object.</span></span>
<span data-ttu-id="3dd04-111">DNS 伺服器具有指定的位址和易記名稱 Dns01。</span><span class="sxs-lookup"><span data-stu-id="3dd04-111">The DNS server has the specified address and the friendly name Dns01.</span></span>
<span data-ttu-id="3dd04-112">該命令會將物件儲存在 $Dns 變數中，以供 **新的 add-azurevm** Cmdlet 使用。</span><span class="sxs-lookup"><span data-stu-id="3dd04-112">The command stores the object in the $Dns variable for use by the **New-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="3dd04-113">參數</span><span class="sxs-lookup"><span data-stu-id="3dd04-113">PARAMETERS</span></span>

### <span data-ttu-id="3dd04-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3dd04-114">-InformationAction</span></span>
<span data-ttu-id="3dd04-115">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="3dd04-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3dd04-116">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3dd04-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3dd04-117">持續</span><span class="sxs-lookup"><span data-stu-id="3dd04-117">Continue</span></span>
- <span data-ttu-id="3dd04-118">理會</span><span class="sxs-lookup"><span data-stu-id="3dd04-118">Ignore</span></span>
- <span data-ttu-id="3dd04-119">看</span><span class="sxs-lookup"><span data-stu-id="3dd04-119">Inquire</span></span>
- <span data-ttu-id="3dd04-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3dd04-120">SilentlyContinue</span></span>
- <span data-ttu-id="3dd04-121">停止</span><span class="sxs-lookup"><span data-stu-id="3dd04-121">Stop</span></span>
- <span data-ttu-id="3dd04-122">封存</span><span class="sxs-lookup"><span data-stu-id="3dd04-122">Suspend</span></span>

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

### <span data-ttu-id="3dd04-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3dd04-123">-InformationVariable</span></span>
<span data-ttu-id="3dd04-124">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="3dd04-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3dd04-125">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="3dd04-125">-IPAddress</span></span>
<span data-ttu-id="3dd04-126">指定 DNS 伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="3dd04-126">Specifies the IP address of the DNS server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dd04-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="3dd04-127">-Name</span></span>
<span data-ttu-id="3dd04-128">指定 DNS 伺服器的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="3dd04-128">Specifies a friendly name for the DNS server.</span></span>
<span data-ttu-id="3dd04-129">這個名稱不一定是完整的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="3dd04-129">This name is not necessarily a fully qualified domain name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dd04-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dd04-130">CommonParameters</span></span>
<span data-ttu-id="3dd04-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3dd04-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dd04-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3dd04-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dd04-133">輸入</span><span class="sxs-lookup"><span data-stu-id="3dd04-133">INPUTS</span></span>

## <span data-ttu-id="3dd04-134">輸出</span><span class="sxs-lookup"><span data-stu-id="3dd04-134">OUTPUTS</span></span>

## <span data-ttu-id="3dd04-135">筆記</span><span class="sxs-lookup"><span data-stu-id="3dd04-135">NOTES</span></span>

## <span data-ttu-id="3dd04-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="3dd04-136">RELATED LINKS</span></span>

[<span data-ttu-id="3dd04-137">附加 AzureDns</span><span class="sxs-lookup"><span data-stu-id="3dd04-137">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="3dd04-138">AzureDns</span><span class="sxs-lookup"><span data-stu-id="3dd04-138">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="3dd04-139">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="3dd04-139">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="3dd04-140">移除-AzureDns</span><span class="sxs-lookup"><span data-stu-id="3dd04-140">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="3dd04-141">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="3dd04-141">Set-AzureDns</span></span>](./Set-AzureDns.md)


