---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1B1C1459-A602-423D-8CAA-B4901CFC2C82
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f684908e8119da007f8b1f844ebbac40713d51
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967925"
---
# <span data-ttu-id="c7184-101">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="c7184-101">Remove-AzureDns</span></span>

## <span data-ttu-id="c7184-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c7184-102">SYNOPSIS</span></span>
<span data-ttu-id="c7184-103">從 Azure 服務移除 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="c7184-103">Removes a DNS server from an Azure service.</span></span>

## <span data-ttu-id="c7184-104">句法</span><span class="sxs-lookup"><span data-stu-id="c7184-104">SYNTAX</span></span>

```
Remove-AzureDns [-Name] <String> [-ServiceName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c7184-105">說明</span><span class="sxs-lookup"><span data-stu-id="c7184-105">DESCRIPTION</span></span>
<span data-ttu-id="c7184-106">**AzureDns** Cmdlet 會從 Azure 服務中移除 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="c7184-106">The **Remove-AzureDns** cmdlet removes a DNS server from an Azure service.</span></span>

## <span data-ttu-id="c7184-107">示例</span><span class="sxs-lookup"><span data-stu-id="c7184-107">EXAMPLES</span></span>

### <span data-ttu-id="c7184-108">範例1：從服務移除 DNS 伺服器</span><span class="sxs-lookup"><span data-stu-id="c7184-108">Example 1: Remove a DNS server from a service</span></span>
```
PS C:\> Remove-AzureDns -ServiceName "ContosoService" -Name "Dns07"
```

<span data-ttu-id="c7184-109">這個命令會從 ContosoService 中移除名為 Dns07 的 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="c7184-109">This command removes the DNS server named Dns07 from ContosoService.</span></span>

## <span data-ttu-id="c7184-110">參數</span><span class="sxs-lookup"><span data-stu-id="c7184-110">PARAMETERS</span></span>

### <span data-ttu-id="c7184-111">-Force</span><span class="sxs-lookup"><span data-stu-id="c7184-111">-Force</span></span>
<span data-ttu-id="c7184-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="c7184-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7184-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c7184-113">-InformationAction</span></span>
<span data-ttu-id="c7184-114">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="c7184-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c7184-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c7184-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c7184-116">持續</span><span class="sxs-lookup"><span data-stu-id="c7184-116">Continue</span></span>
- <span data-ttu-id="c7184-117">理會</span><span class="sxs-lookup"><span data-stu-id="c7184-117">Ignore</span></span>
- <span data-ttu-id="c7184-118">看</span><span class="sxs-lookup"><span data-stu-id="c7184-118">Inquire</span></span>
- <span data-ttu-id="c7184-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c7184-119">SilentlyContinue</span></span>
- <span data-ttu-id="c7184-120">停止</span><span class="sxs-lookup"><span data-stu-id="c7184-120">Stop</span></span>
- <span data-ttu-id="c7184-121">封存</span><span class="sxs-lookup"><span data-stu-id="c7184-121">Suspend</span></span>

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

### <span data-ttu-id="c7184-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c7184-122">-InformationVariable</span></span>
<span data-ttu-id="c7184-123">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="c7184-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c7184-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="c7184-124">-Name</span></span>
<span data-ttu-id="c7184-125">指定此 Cmdlet 移除的 DNS 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="c7184-125">Specifies the name of the DNS server that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c7184-126">-設定檔</span><span class="sxs-lookup"><span data-stu-id="c7184-126">-Profile</span></span>
<span data-ttu-id="c7184-127">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="c7184-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c7184-128">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="c7184-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c7184-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c7184-129">-ServiceName</span></span>
<span data-ttu-id="c7184-130">指定此 Cmdlet 從中移除 DNS 伺服器的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="c7184-130">Specifies the name of the service from which this cmdlet removes a DNS server.</span></span>

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

### <span data-ttu-id="c7184-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7184-131">CommonParameters</span></span>
<span data-ttu-id="c7184-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c7184-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7184-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c7184-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7184-134">輸入</span><span class="sxs-lookup"><span data-stu-id="c7184-134">INPUTS</span></span>

## <span data-ttu-id="c7184-135">輸出</span><span class="sxs-lookup"><span data-stu-id="c7184-135">OUTPUTS</span></span>

### <span data-ttu-id="c7184-136">WindowsAzure. 常見. ManagementOperationCoNtext</span><span class="sxs-lookup"><span data-stu-id="c7184-136">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="c7184-137">筆記</span><span class="sxs-lookup"><span data-stu-id="c7184-137">NOTES</span></span>

## <span data-ttu-id="c7184-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="c7184-138">RELATED LINKS</span></span>

[<span data-ttu-id="c7184-139">附加 AzureDns</span><span class="sxs-lookup"><span data-stu-id="c7184-139">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="c7184-140">AzureDns</span><span class="sxs-lookup"><span data-stu-id="c7184-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="c7184-141">新-AzureDns</span><span class="sxs-lookup"><span data-stu-id="c7184-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="c7184-142">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="c7184-142">Set-AzureDns</span></span>](./Set-AzureDns.md)


