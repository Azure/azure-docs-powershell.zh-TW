---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5BC16303-CCB4-40D8-ABCB-59CF0D85ED63
online version: ''
schema: 2.0.0
ms.openlocfilehash: f24f5d8f7f72c59847cfa5dde51a1937bc304735
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967515"
---
# <span data-ttu-id="3b723-101">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="3b723-101">Set-AzureDns</span></span>

## <span data-ttu-id="3b723-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3b723-102">SYNOPSIS</span></span>
<span data-ttu-id="3b723-103">修改 DNS 伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="3b723-103">Modifies the IP address of a DNS server.</span></span>

## <span data-ttu-id="3b723-104">句法</span><span class="sxs-lookup"><span data-stu-id="3b723-104">SYNTAX</span></span>

```
Set-AzureDns [-Name] <String> [-IPAddress] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3b723-105">說明</span><span class="sxs-lookup"><span data-stu-id="3b723-105">DESCRIPTION</span></span>
<span data-ttu-id="3b723-106">**AzureDns** Cmdlet 會修改 Azure 服務之 DNS 伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="3b723-106">The **Set-AzureDns** cmdlet modifies the IP address of a DNS server for an Azure service.</span></span>

## <span data-ttu-id="3b723-107">示例</span><span class="sxs-lookup"><span data-stu-id="3b723-107">EXAMPLES</span></span>

### <span data-ttu-id="3b723-108">範例1：修改 DNS 伺服器的 IP 位址</span><span class="sxs-lookup"><span data-stu-id="3b723-108">Example 1: Modify the IP address of a DNS server</span></span>
```
PS C:\> Set-AzureDns -ServiceName "ContosoService" -IPAddress 10.1.2.5 -Name "Dns07"
```

<span data-ttu-id="3b723-109">這個命令會修改名為 ContosoService 之服務之名為 Dns07 的 DNS 伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="3b723-109">This command modifies the IP address of the DNS server named Dns07 for the service named ContosoService.</span></span>

## <span data-ttu-id="3b723-110">參數</span><span class="sxs-lookup"><span data-stu-id="3b723-110">PARAMETERS</span></span>

### <span data-ttu-id="3b723-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3b723-111">-InformationAction</span></span>
<span data-ttu-id="3b723-112">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="3b723-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3b723-113">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3b723-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3b723-114">持續</span><span class="sxs-lookup"><span data-stu-id="3b723-114">Continue</span></span>
- <span data-ttu-id="3b723-115">理會</span><span class="sxs-lookup"><span data-stu-id="3b723-115">Ignore</span></span>
- <span data-ttu-id="3b723-116">看</span><span class="sxs-lookup"><span data-stu-id="3b723-116">Inquire</span></span>
- <span data-ttu-id="3b723-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3b723-117">SilentlyContinue</span></span>
- <span data-ttu-id="3b723-118">停止</span><span class="sxs-lookup"><span data-stu-id="3b723-118">Stop</span></span>
- <span data-ttu-id="3b723-119">封存</span><span class="sxs-lookup"><span data-stu-id="3b723-119">Suspend</span></span>

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

### <span data-ttu-id="3b723-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3b723-120">-InformationVariable</span></span>
<span data-ttu-id="3b723-121">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="3b723-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3b723-122">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="3b723-122">-IPAddress</span></span>
<span data-ttu-id="3b723-123">指定 DNS 伺服器的新 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="3b723-123">Specifies the new IP address of the DNS server.</span></span>

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

### <span data-ttu-id="3b723-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="3b723-124">-Name</span></span>
<span data-ttu-id="3b723-125">指定此 Cmdlet 所修改之 DNS 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b723-125">Specifies the name of the DNS server that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3b723-126">-設定檔</span><span class="sxs-lookup"><span data-stu-id="3b723-126">-Profile</span></span>
<span data-ttu-id="3b723-127">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="3b723-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3b723-128">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="3b723-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3b723-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3b723-129">-ServiceName</span></span>
<span data-ttu-id="3b723-130">指定此 Cmdlet 修改 DNS 伺服器位址的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="3b723-130">Specifies the name of the service for which this cmdlet modifies the address of the DNS server.</span></span>

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

### <span data-ttu-id="3b723-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b723-131">CommonParameters</span></span>
<span data-ttu-id="3b723-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3b723-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b723-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3b723-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b723-134">輸入</span><span class="sxs-lookup"><span data-stu-id="3b723-134">INPUTS</span></span>

## <span data-ttu-id="3b723-135">輸出</span><span class="sxs-lookup"><span data-stu-id="3b723-135">OUTPUTS</span></span>

### <span data-ttu-id="3b723-136">WindowsAzure. 常見. ManagementOperationCoNtext</span><span class="sxs-lookup"><span data-stu-id="3b723-136">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="3b723-137">筆記</span><span class="sxs-lookup"><span data-stu-id="3b723-137">NOTES</span></span>

## <span data-ttu-id="3b723-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b723-138">RELATED LINKS</span></span>

[<span data-ttu-id="3b723-139">附加 AzureDns</span><span class="sxs-lookup"><span data-stu-id="3b723-139">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="3b723-140">AzureDns</span><span class="sxs-lookup"><span data-stu-id="3b723-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="3b723-141">新-AzureDns</span><span class="sxs-lookup"><span data-stu-id="3b723-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="3b723-142">移除-AzureDns</span><span class="sxs-lookup"><span data-stu-id="3b723-142">Remove-AzureDns</span></span>](./Remove-AzureDns.md)


