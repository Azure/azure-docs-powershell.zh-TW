---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 184FB33A-C866-4AF0-BA31-8ADCFC6EE8E2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 15ce5d8511383ad93e288b97381416d7864c3f80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967092"
---
# <span data-ttu-id="021b2-101">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="021b2-101">Get-AzureDns</span></span>

## <span data-ttu-id="021b2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="021b2-102">SYNOPSIS</span></span>
<span data-ttu-id="021b2-103">取得 Azure 部署的 DNS 設定。</span><span class="sxs-lookup"><span data-stu-id="021b2-103">Gets the DNS settings for an Azure deployment.</span></span>

## <span data-ttu-id="021b2-104">句法</span><span class="sxs-lookup"><span data-stu-id="021b2-104">SYNTAX</span></span>

```
Get-AzureDns [-DnsSettings <DnsSettings>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="021b2-105">說明</span><span class="sxs-lookup"><span data-stu-id="021b2-105">DESCRIPTION</span></span>
<span data-ttu-id="021b2-106">**AzureDns** Cmdlet 會取得 Azure 部署的 DNS 設定。</span><span class="sxs-lookup"><span data-stu-id="021b2-106">The **Get-AzureDns** cmdlet gets the DNS settings for an Azure deployment.</span></span>
<span data-ttu-id="021b2-107">Cmdlet 會在 DNS 設定物件中傳回 DNS 伺服器的易記名稱和 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="021b2-107">The cmdlet returns the friendly name and IP address of the DNS server in a DNS settings object.</span></span>

## <span data-ttu-id="021b2-108">示例</span><span class="sxs-lookup"><span data-stu-id="021b2-108">EXAMPLES</span></span>

### <span data-ttu-id="021b2-109">範例1：取得 DNS 設定</span><span class="sxs-lookup"><span data-stu-id="021b2-109">Example 1: Get DNS settings</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService" -Slot "Production" | Get-AzureDNS
```

<span data-ttu-id="021b2-110">這個命令會使用 **AzureDeployment** Cmdlet 來取得服務的生產部署（名為 ContosoService）。</span><span class="sxs-lookup"><span data-stu-id="021b2-110">This command uses the **Get-AzureDeployment** cmdlet to get the production deployment of the service named ContosoService.</span></span>
<span data-ttu-id="021b2-111">命令會使用管線運算子，將該物件傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="021b2-111">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="021b2-112">目前的 Cmdlet 會取得 DNS 設定。</span><span class="sxs-lookup"><span data-stu-id="021b2-112">The current cmdlet gets the DNS settings.</span></span>

## <span data-ttu-id="021b2-113">參數</span><span class="sxs-lookup"><span data-stu-id="021b2-113">PARAMETERS</span></span>

### <span data-ttu-id="021b2-114">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="021b2-114">-DnsSettings</span></span>
<span data-ttu-id="021b2-115">指定 **DnsSettings** 物件。</span><span class="sxs-lookup"><span data-stu-id="021b2-115">Specifies a **DnsSettings** object.</span></span>

```yaml
Type: DnsSettings
Parameter Sets: (All)
Aliases: InputObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="021b2-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="021b2-116">-InformationAction</span></span>
<span data-ttu-id="021b2-117">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="021b2-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="021b2-118">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="021b2-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="021b2-119">持續</span><span class="sxs-lookup"><span data-stu-id="021b2-119">Continue</span></span>
- <span data-ttu-id="021b2-120">理會</span><span class="sxs-lookup"><span data-stu-id="021b2-120">Ignore</span></span>
- <span data-ttu-id="021b2-121">看</span><span class="sxs-lookup"><span data-stu-id="021b2-121">Inquire</span></span>
- <span data-ttu-id="021b2-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="021b2-122">SilentlyContinue</span></span>
- <span data-ttu-id="021b2-123">停止</span><span class="sxs-lookup"><span data-stu-id="021b2-123">Stop</span></span>
- <span data-ttu-id="021b2-124">封存</span><span class="sxs-lookup"><span data-stu-id="021b2-124">Suspend</span></span>

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

### <span data-ttu-id="021b2-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="021b2-125">-InformationVariable</span></span>
<span data-ttu-id="021b2-126">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="021b2-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="021b2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="021b2-127">CommonParameters</span></span>
<span data-ttu-id="021b2-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="021b2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="021b2-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="021b2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="021b2-130">輸入</span><span class="sxs-lookup"><span data-stu-id="021b2-130">INPUTS</span></span>

## <span data-ttu-id="021b2-131">輸出</span><span class="sxs-lookup"><span data-stu-id="021b2-131">OUTPUTS</span></span>

## <span data-ttu-id="021b2-132">筆記</span><span class="sxs-lookup"><span data-stu-id="021b2-132">NOTES</span></span>

## <span data-ttu-id="021b2-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="021b2-133">RELATED LINKS</span></span>

[<span data-ttu-id="021b2-134">附加 AzureDns</span><span class="sxs-lookup"><span data-stu-id="021b2-134">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="021b2-135">AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="021b2-135">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="021b2-136">新-AzureDns</span><span class="sxs-lookup"><span data-stu-id="021b2-136">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="021b2-137">移除-AzureDns</span><span class="sxs-lookup"><span data-stu-id="021b2-137">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="021b2-138">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="021b2-138">Set-AzureDns</span></span>](./Set-AzureDns.md)


