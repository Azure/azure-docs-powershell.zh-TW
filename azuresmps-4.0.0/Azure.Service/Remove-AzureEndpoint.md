---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5A068EC9-3745-4219-BA03-C56CB9D9D157
online version: ''
schema: 2.0.0
ms.openlocfilehash: 24fad9fc499c3f7abec5e7539fd1e221835849ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967924"
---
# <span data-ttu-id="bf845-101">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf845-101">Remove-AzureEndpoint</span></span>

## <span data-ttu-id="bf845-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bf845-102">SYNOPSIS</span></span>
<span data-ttu-id="bf845-103">從 Azure 虛擬機器刪除端點。</span><span class="sxs-lookup"><span data-stu-id="bf845-103">Deletes an endpoint from an Azure virtual machine.</span></span>

## <span data-ttu-id="bf845-104">句法</span><span class="sxs-lookup"><span data-stu-id="bf845-104">SYNTAX</span></span>

```
Remove-AzureEndpoint [-Name] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="bf845-105">說明</span><span class="sxs-lookup"><span data-stu-id="bf845-105">DESCRIPTION</span></span>
<span data-ttu-id="bf845-106">**AzureEndpoint** Cmdlet 會從 Azure 虛擬機器物件中刪除端點。</span><span class="sxs-lookup"><span data-stu-id="bf845-106">The **Remove-AzureEndpoint** cmdlet deletes an endpoint from an Azure virtual machine object.</span></span>

## <span data-ttu-id="bf845-107">示例</span><span class="sxs-lookup"><span data-stu-id="bf845-107">EXAMPLES</span></span>

### <span data-ttu-id="bf845-108">範例1：移除端點</span><span class="sxs-lookup"><span data-stu-id="bf845-108">Example 1: Remove an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine01" | Remove-AzureEndpoint -Name "HttpIn" | Update-AzureVM
```

<span data-ttu-id="bf845-109">這個命令會使用 **add-azurevm** Cmdlet 來檢索名為 VirtualMachine01 的虛擬機器的設定。</span><span class="sxs-lookup"><span data-stu-id="bf845-109">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="bf845-110">命令會使用管線運算子將它傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bf845-110">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bf845-111">這個 Cmdlet 會移除一個名為 HttpIn 的端點。</span><span class="sxs-lookup"><span data-stu-id="bf845-111">This cmdlet removes an endpoint named HttpIn.</span></span>
<span data-ttu-id="bf845-112">該命令會將虛擬機器物件傳遞到會實現變更的 **add-azurevm** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bf845-112">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

## <span data-ttu-id="bf845-113">參數</span><span class="sxs-lookup"><span data-stu-id="bf845-113">PARAMETERS</span></span>

### <span data-ttu-id="bf845-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="bf845-114">-InformationAction</span></span>
<span data-ttu-id="bf845-115">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="bf845-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bf845-116">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="bf845-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bf845-117">持續</span><span class="sxs-lookup"><span data-stu-id="bf845-117">Continue</span></span>
- <span data-ttu-id="bf845-118">理會</span><span class="sxs-lookup"><span data-stu-id="bf845-118">Ignore</span></span>
- <span data-ttu-id="bf845-119">看</span><span class="sxs-lookup"><span data-stu-id="bf845-119">Inquire</span></span>
- <span data-ttu-id="bf845-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bf845-120">SilentlyContinue</span></span>
- <span data-ttu-id="bf845-121">停止</span><span class="sxs-lookup"><span data-stu-id="bf845-121">Stop</span></span>
- <span data-ttu-id="bf845-122">封存</span><span class="sxs-lookup"><span data-stu-id="bf845-122">Suspend</span></span>

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

### <span data-ttu-id="bf845-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bf845-123">-InformationVariable</span></span>
<span data-ttu-id="bf845-124">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="bf845-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bf845-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="bf845-125">-Name</span></span>
<span data-ttu-id="bf845-126">指定此 Cmdlet 從虛擬機器中刪除之端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf845-126">Specifies the name of the endpoint that this cmdlet deletes from the virtual machine.</span></span>

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

### <span data-ttu-id="bf845-127">-設定檔</span><span class="sxs-lookup"><span data-stu-id="bf845-127">-Profile</span></span>
<span data-ttu-id="bf845-128">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="bf845-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bf845-129">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="bf845-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bf845-130">-VM</span><span class="sxs-lookup"><span data-stu-id="bf845-130">-VM</span></span>
<span data-ttu-id="bf845-131">指定此 Cmdlet 刪除端點的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="bf845-131">Specifies the virtual machine from which this cmdlet deletes an endpoint.</span></span>

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

### <span data-ttu-id="bf845-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf845-132">CommonParameters</span></span>
<span data-ttu-id="bf845-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bf845-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf845-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bf845-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf845-135">輸入</span><span class="sxs-lookup"><span data-stu-id="bf845-135">INPUTS</span></span>

## <span data-ttu-id="bf845-136">輸出</span><span class="sxs-lookup"><span data-stu-id="bf845-136">OUTPUTS</span></span>

## <span data-ttu-id="bf845-137">筆記</span><span class="sxs-lookup"><span data-stu-id="bf845-137">NOTES</span></span>

## <span data-ttu-id="bf845-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="bf845-138">RELATED LINKS</span></span>

[<span data-ttu-id="bf845-139">附加 AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf845-139">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="bf845-140">AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf845-140">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="bf845-141">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="bf845-141">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="bf845-142">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf845-142">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="bf845-143">更新-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="bf845-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


