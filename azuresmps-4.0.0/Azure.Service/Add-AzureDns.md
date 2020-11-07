---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: AF4DF7EC-95BA-44E2-AB9B-5C8FE45CCE4C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83c0858d813c157301098f680fa9d2a90ef6950a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967180"
---
# <span data-ttu-id="440cf-101">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="440cf-101">Add-AzureDns</span></span>

## <span data-ttu-id="440cf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="440cf-102">SYNOPSIS</span></span>
<span data-ttu-id="440cf-103">將 DNS 伺服器新增至 Azure 服務。</span><span class="sxs-lookup"><span data-stu-id="440cf-103">Adds a DNS server to an Azure service.</span></span>

## <span data-ttu-id="440cf-104">句法</span><span class="sxs-lookup"><span data-stu-id="440cf-104">SYNTAX</span></span>

```
Add-AzureDns [-Name] <String> [-IPAddress] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="440cf-105">說明</span><span class="sxs-lookup"><span data-stu-id="440cf-105">DESCRIPTION</span></span>
<span data-ttu-id="440cf-106">**AzureDns** Cmdlet 會將 DNS 伺服器新增至 Azure 服務。</span><span class="sxs-lookup"><span data-stu-id="440cf-106">The **Add-AzureDns** cmdlet adds a DNS server to an Azure service.</span></span>

## <span data-ttu-id="440cf-107">示例</span><span class="sxs-lookup"><span data-stu-id="440cf-107">EXAMPLES</span></span>

### <span data-ttu-id="440cf-108">範例1：新增 DNS 伺服器</span><span class="sxs-lookup"><span data-stu-id="440cf-108">Example 1: Add a DNS server</span></span>
```
PS C:\> Add-AzureDns -ServiceName "ContosoService" -IPAddress 10.1.2.4 -Name "Dns07"
```

<span data-ttu-id="440cf-109">這個命令會將具有位址10.1.2.4 的 DNS 伺服器新增到 ContosoService。</span><span class="sxs-lookup"><span data-stu-id="440cf-109">This command adds the DNS server that has the address 10.1.2.4 to ContosoService.</span></span>

## <span data-ttu-id="440cf-110">參數</span><span class="sxs-lookup"><span data-stu-id="440cf-110">PARAMETERS</span></span>

### <span data-ttu-id="440cf-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="440cf-111">-InformationAction</span></span>
<span data-ttu-id="440cf-112">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="440cf-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="440cf-113">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="440cf-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="440cf-114">持續</span><span class="sxs-lookup"><span data-stu-id="440cf-114">Continue</span></span>
- <span data-ttu-id="440cf-115">理會</span><span class="sxs-lookup"><span data-stu-id="440cf-115">Ignore</span></span>
- <span data-ttu-id="440cf-116">看</span><span class="sxs-lookup"><span data-stu-id="440cf-116">Inquire</span></span>
- <span data-ttu-id="440cf-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="440cf-117">SilentlyContinue</span></span>
- <span data-ttu-id="440cf-118">停止</span><span class="sxs-lookup"><span data-stu-id="440cf-118">Stop</span></span>
- <span data-ttu-id="440cf-119">封存</span><span class="sxs-lookup"><span data-stu-id="440cf-119">Suspend</span></span>

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

### <span data-ttu-id="440cf-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="440cf-120">-InformationVariable</span></span>
<span data-ttu-id="440cf-121">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="440cf-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="440cf-122">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="440cf-122">-IPAddress</span></span>
<span data-ttu-id="440cf-123">指定 DNS 伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="440cf-123">Specifies the IP address of the DNS server.</span></span>

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

### <span data-ttu-id="440cf-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="440cf-124">-Name</span></span>
<span data-ttu-id="440cf-125">指定 DNS 伺服器的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="440cf-125">Specifies a friendly name for the DNS server.</span></span>
<span data-ttu-id="440cf-126">這個名稱不一定是完整的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="440cf-126">This name is not necessarily a fully qualified domain name.</span></span>

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

### <span data-ttu-id="440cf-127">-設定檔</span><span class="sxs-lookup"><span data-stu-id="440cf-127">-Profile</span></span>
<span data-ttu-id="440cf-128">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="440cf-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="440cf-129">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="440cf-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="440cf-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="440cf-130">-ServiceName</span></span>
<span data-ttu-id="440cf-131">指定此 Cmdlet 新增 DNS 伺服器的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="440cf-131">Specifies the name of the service to which this cmdlet adds the DNS server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="440cf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="440cf-132">CommonParameters</span></span>
<span data-ttu-id="440cf-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="440cf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="440cf-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="440cf-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="440cf-135">輸入</span><span class="sxs-lookup"><span data-stu-id="440cf-135">INPUTS</span></span>

## <span data-ttu-id="440cf-136">輸出</span><span class="sxs-lookup"><span data-stu-id="440cf-136">OUTPUTS</span></span>

### <span data-ttu-id="440cf-137">WindowsAzure. 常見. ManagementOperationCoNtext</span><span class="sxs-lookup"><span data-stu-id="440cf-137">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="440cf-138">筆記</span><span class="sxs-lookup"><span data-stu-id="440cf-138">NOTES</span></span>

## <span data-ttu-id="440cf-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="440cf-139">RELATED LINKS</span></span>

[<span data-ttu-id="440cf-140">AzureDns</span><span class="sxs-lookup"><span data-stu-id="440cf-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="440cf-141">新-AzureDns</span><span class="sxs-lookup"><span data-stu-id="440cf-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="440cf-142">移除-AzureDns</span><span class="sxs-lookup"><span data-stu-id="440cf-142">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="440cf-143">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="440cf-143">Set-AzureDns</span></span>](./Set-AzureDns.md)


