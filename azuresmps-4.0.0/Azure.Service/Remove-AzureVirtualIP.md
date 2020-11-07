---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B107D789-8F66-4D7D-B126-08ACB0364826
online version: ''
schema: 2.0.0
ms.openlocfilehash: e59df078539e9ea94073defd4c8ea13a69cc2e5f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966933"
---
# <span data-ttu-id="f9876-101">Remove-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="f9876-101">Remove-AzureVirtualIP</span></span>

## <span data-ttu-id="f9876-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f9876-102">SYNOPSIS</span></span>
<span data-ttu-id="f9876-103">從您的雲端服務刪除虛擬 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f9876-103">Deletes a virtual IP address from your Cloud Service.</span></span>

## <span data-ttu-id="f9876-104">句法</span><span class="sxs-lookup"><span data-stu-id="f9876-104">SYNTAX</span></span>

```
Remove-AzureVirtualIP [-ServiceName] <String> [-VirtualIPName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f9876-105">說明</span><span class="sxs-lookup"><span data-stu-id="f9876-105">DESCRIPTION</span></span>
<span data-ttu-id="f9876-106">**AzureVirtualIP** Cmdlet 會從 Azure 服務刪除虛擬 IP (VIP) 。</span><span class="sxs-lookup"><span data-stu-id="f9876-106">The **Remove-AzureVirtualIP** cmdlet deletes a virtual IP (VIP) from an Azure service.</span></span>
<span data-ttu-id="f9876-107">只有虛擬 IP 沒有關聯的端點，作業才會成功。</span><span class="sxs-lookup"><span data-stu-id="f9876-107">The operation succeeds only if the virtual IP has no endpoints associated with it.</span></span>

## <span data-ttu-id="f9876-108">示例</span><span class="sxs-lookup"><span data-stu-id="f9876-108">EXAMPLES</span></span>

### <span data-ttu-id="f9876-109">範例1：從服務移除虛擬 IP 位址</span><span class="sxs-lookup"><span data-stu-id="f9876-109">Example 1: Remove a virtual IP address from a service</span></span>
```
PS C:\> Remove-AzureVirtualIP -VirtualIPName "Vip01" -ServiceName "ContosoService03"
```

<span data-ttu-id="f9876-110">這個命令會從服務中移除虛擬 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f9876-110">This command removes a virtual IP address from a service.</span></span>

## <span data-ttu-id="f9876-111">參數</span><span class="sxs-lookup"><span data-stu-id="f9876-111">PARAMETERS</span></span>

### <span data-ttu-id="f9876-112">-Force</span><span class="sxs-lookup"><span data-stu-id="f9876-112">-Force</span></span>
<span data-ttu-id="f9876-113">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="f9876-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9876-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f9876-114">-InformationAction</span></span>
<span data-ttu-id="f9876-115">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="f9876-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f9876-116">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f9876-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f9876-117">持續</span><span class="sxs-lookup"><span data-stu-id="f9876-117">Continue</span></span>
- <span data-ttu-id="f9876-118">理會</span><span class="sxs-lookup"><span data-stu-id="f9876-118">Ignore</span></span>
- <span data-ttu-id="f9876-119">看</span><span class="sxs-lookup"><span data-stu-id="f9876-119">Inquire</span></span>
- <span data-ttu-id="f9876-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f9876-120">SilentlyContinue</span></span>
- <span data-ttu-id="f9876-121">停止</span><span class="sxs-lookup"><span data-stu-id="f9876-121">Stop</span></span>
- <span data-ttu-id="f9876-122">封存</span><span class="sxs-lookup"><span data-stu-id="f9876-122">Suspend</span></span>

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

### <span data-ttu-id="f9876-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f9876-123">-InformationVariable</span></span>
<span data-ttu-id="f9876-124">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="f9876-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f9876-125">-設定檔</span><span class="sxs-lookup"><span data-stu-id="f9876-125">-Profile</span></span>
<span data-ttu-id="f9876-126">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="f9876-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f9876-127">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="f9876-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f9876-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f9876-128">-ServiceName</span></span>
<span data-ttu-id="f9876-129">指定要從中移除虛擬 IP 位址的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="f9876-129">Specifies the name of the service from which to remove a virtual IP address.</span></span>

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

### <span data-ttu-id="f9876-130">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="f9876-130">-VirtualIPName</span></span>
<span data-ttu-id="f9876-131">指定要移除之虛擬 IP 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9876-131">Specifies the name of the virtual IP address to remove.</span></span>

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

### <span data-ttu-id="f9876-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9876-132">CommonParameters</span></span>
<span data-ttu-id="f9876-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f9876-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9876-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f9876-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9876-135">輸入</span><span class="sxs-lookup"><span data-stu-id="f9876-135">INPUTS</span></span>

## <span data-ttu-id="f9876-136">輸出</span><span class="sxs-lookup"><span data-stu-id="f9876-136">OUTPUTS</span></span>

### <span data-ttu-id="f9876-137">WindowsAzure. 常見. ManagementOperationCoNtext</span><span class="sxs-lookup"><span data-stu-id="f9876-137">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="f9876-138">筆記</span><span class="sxs-lookup"><span data-stu-id="f9876-138">NOTES</span></span>

## <span data-ttu-id="f9876-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9876-139">RELATED LINKS</span></span>

[<span data-ttu-id="f9876-140">附加 AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="f9876-140">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)


