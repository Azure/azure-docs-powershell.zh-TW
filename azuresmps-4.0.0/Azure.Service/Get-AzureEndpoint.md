---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1CFB90FD-7BC5-4687-8D08-775097DDA062
online version: ''
schema: 2.0.0
ms.openlocfilehash: 651b38a21dff03ce3c5925040d65bc2967eeaa77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967091"
---
# <span data-ttu-id="b8667-101">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="b8667-101">Get-AzureEndpoint</span></span>

## <span data-ttu-id="b8667-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b8667-102">SYNOPSIS</span></span>
<span data-ttu-id="b8667-103">取得指派給 Azure 虛擬機器之端點的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b8667-103">Gets information about the endpoints that are assigned to an Azure virtual machine.</span></span>

## <span data-ttu-id="b8667-104">句法</span><span class="sxs-lookup"><span data-stu-id="b8667-104">SYNTAX</span></span>

```
Get-AzureEndpoint [[-Name] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b8667-105">說明</span><span class="sxs-lookup"><span data-stu-id="b8667-105">DESCRIPTION</span></span>
<span data-ttu-id="b8667-106">**AzureEndpoint** Cmdlet 會取得指派給 Azure 虛擬機器之端點的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b8667-106">The **Get-AzureEndpoint** cmdlet gets information about the endpoints that are assigned to an Azure virtual machine.</span></span>

## <span data-ttu-id="b8667-107">示例</span><span class="sxs-lookup"><span data-stu-id="b8667-107">EXAMPLES</span></span>

### <span data-ttu-id="b8667-108">範例1：取得虛擬機器的端點資訊</span><span class="sxs-lookup"><span data-stu-id="b8667-108">Example 1: Get endpoint information for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine12" | Get-AzureEndpoint
```

<span data-ttu-id="b8667-109">這個命令會使用 **add-azurevm** Cmdlet 來檢索名為 VirtualMachine12 的虛擬機器的設定。</span><span class="sxs-lookup"><span data-stu-id="b8667-109">This command retrieves the configuration of a virtual machine named VirtualMachine12 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="b8667-110">命令會使用管線運算子將它傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b8667-110">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b8667-111">這個 Cmdlet 會取得該虛擬機器的端點資訊。</span><span class="sxs-lookup"><span data-stu-id="b8667-111">This cmdlet gets endpoint information for that virtual machine.</span></span>

## <span data-ttu-id="b8667-112">參數</span><span class="sxs-lookup"><span data-stu-id="b8667-112">PARAMETERS</span></span>

### <span data-ttu-id="b8667-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b8667-113">-InformationAction</span></span>
<span data-ttu-id="b8667-114">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="b8667-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b8667-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b8667-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b8667-116">持續</span><span class="sxs-lookup"><span data-stu-id="b8667-116">Continue</span></span>
- <span data-ttu-id="b8667-117">理會</span><span class="sxs-lookup"><span data-stu-id="b8667-117">Ignore</span></span>
- <span data-ttu-id="b8667-118">看</span><span class="sxs-lookup"><span data-stu-id="b8667-118">Inquire</span></span>
- <span data-ttu-id="b8667-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b8667-119">SilentlyContinue</span></span>
- <span data-ttu-id="b8667-120">停止</span><span class="sxs-lookup"><span data-stu-id="b8667-120">Stop</span></span>
- <span data-ttu-id="b8667-121">封存</span><span class="sxs-lookup"><span data-stu-id="b8667-121">Suspend</span></span>

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

### <span data-ttu-id="b8667-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b8667-122">-InformationVariable</span></span>
<span data-ttu-id="b8667-123">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="b8667-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b8667-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="b8667-124">-Name</span></span>
<span data-ttu-id="b8667-125">指定此 Cmdlet 取得資訊之端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8667-125">Specifies the name of the endpoint for which this cmdlet gets information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8667-126">-設定檔</span><span class="sxs-lookup"><span data-stu-id="b8667-126">-Profile</span></span>
<span data-ttu-id="b8667-127">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b8667-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b8667-128">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="b8667-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b8667-129">-VM</span><span class="sxs-lookup"><span data-stu-id="b8667-129">-VM</span></span>
<span data-ttu-id="b8667-130">指定此 Cmdlet 取得端點資訊的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b8667-130">Specifies the virtual machine from which this cmdlet gets endpoint information.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8667-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8667-131">CommonParameters</span></span>
<span data-ttu-id="b8667-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b8667-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8667-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b8667-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8667-134">輸入</span><span class="sxs-lookup"><span data-stu-id="b8667-134">INPUTS</span></span>

## <span data-ttu-id="b8667-135">輸出</span><span class="sxs-lookup"><span data-stu-id="b8667-135">OUTPUTS</span></span>

## <span data-ttu-id="b8667-136">筆記</span><span class="sxs-lookup"><span data-stu-id="b8667-136">NOTES</span></span>

## <span data-ttu-id="b8667-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8667-137">RELATED LINKS</span></span>

[<span data-ttu-id="b8667-138">附加 AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="b8667-138">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="b8667-139">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="b8667-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="b8667-140">移除-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="b8667-140">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="b8667-141">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="b8667-141">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)


