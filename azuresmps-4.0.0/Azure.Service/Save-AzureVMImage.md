---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9A1CE31E-0158-441E-BC2D-B5D21C9D9421
online version: ''
schema: 2.0.0
ms.openlocfilehash: a956aa7eaf383b0cf5cdb20b39d2f6b54e292f92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966897"
---
# <span data-ttu-id="20b25-101">Save-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="20b25-101">Save-AzureVMImage</span></span>

## <span data-ttu-id="20b25-102">摘要</span><span class="sxs-lookup"><span data-stu-id="20b25-102">SYNOPSIS</span></span>
<span data-ttu-id="20b25-103">捕獲並儲存已停止之 Azure 虛擬機器的影像。</span><span class="sxs-lookup"><span data-stu-id="20b25-103">Captures and saves the image of a stopped Azure virtual machine.</span></span>

## <span data-ttu-id="20b25-104">句法</span><span class="sxs-lookup"><span data-stu-id="20b25-104">SYNTAX</span></span>

```
Save-AzureVMImage [-ServiceName] <String> [-Name] <String> [-ImageName] <String> [[-ImageLabel] <String>]
 [[-OSState] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="20b25-105">說明</span><span class="sxs-lookup"><span data-stu-id="20b25-105">DESCRIPTION</span></span>
<span data-ttu-id="20b25-106">AzureVMImage Cmdlet 會捕獲並 **儲存** 已停止的 Azure 虛擬機器的影像。</span><span class="sxs-lookup"><span data-stu-id="20b25-106">The **Save-AzureVMImage** cmdlet captures and saves the image of a stopped Azure virtual machine.</span></span>
<span data-ttu-id="20b25-107">如果是 Windows 虛擬機器，請執行 Sysprep 工具，在捕獲前先準備影像。</span><span class="sxs-lookup"><span data-stu-id="20b25-107">For Windows virtual machines, run the Sysprep tool to prepare the image before it is captured.</span></span>
<span data-ttu-id="20b25-108">捕獲影像之後，就會刪除虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="20b25-108">After the image is captured, the virtual machine is deleted.</span></span>

## <span data-ttu-id="20b25-109">示例</span><span class="sxs-lookup"><span data-stu-id="20b25-109">EXAMPLES</span></span>

### <span data-ttu-id="20b25-110">範例1：儲存現有的虛擬機器，然後從部署中刪除</span><span class="sxs-lookup"><span data-stu-id="20b25-110">Example 1: Save an existing virtual machine and then delete it from a deployment</span></span>
```
PS C:\> Save-AzureVMImage -ServiceName "MyService" -Name "MyVM" -NewImageName "MyBaseImage" -NewImageLabel "MyBaseVM"
```

<span data-ttu-id="20b25-111">這個命令會捕獲現有的虛擬機器，並將它從部署中刪除。</span><span class="sxs-lookup"><span data-stu-id="20b25-111">This command captures an existing virtual machine and deletes it from the deployment.</span></span>

## <span data-ttu-id="20b25-112">參數</span><span class="sxs-lookup"><span data-stu-id="20b25-112">PARAMETERS</span></span>

### <span data-ttu-id="20b25-113">-ImageLabel</span><span class="sxs-lookup"><span data-stu-id="20b25-113">-ImageLabel</span></span>
<span data-ttu-id="20b25-114">指定虛擬機器影像的標籤。</span><span class="sxs-lookup"><span data-stu-id="20b25-114">Specifies the label of the virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewImageLabel

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20b25-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="20b25-115">-ImageName</span></span>
<span data-ttu-id="20b25-116">指定虛擬機器影像的名稱。</span><span class="sxs-lookup"><span data-stu-id="20b25-116">Specifies the name of the virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewImageName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20b25-117">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="20b25-117">-InformationAction</span></span>
<span data-ttu-id="20b25-118">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="20b25-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="20b25-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="20b25-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="20b25-120">持續</span><span class="sxs-lookup"><span data-stu-id="20b25-120">Continue</span></span>
- <span data-ttu-id="20b25-121">理會</span><span class="sxs-lookup"><span data-stu-id="20b25-121">Ignore</span></span>
- <span data-ttu-id="20b25-122">看</span><span class="sxs-lookup"><span data-stu-id="20b25-122">Inquire</span></span>
- <span data-ttu-id="20b25-123">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="20b25-123">SilentlyContinue</span></span>
- <span data-ttu-id="20b25-124">停止</span><span class="sxs-lookup"><span data-stu-id="20b25-124">Stop</span></span>
- <span data-ttu-id="20b25-125">封存</span><span class="sxs-lookup"><span data-stu-id="20b25-125">Suspend</span></span>

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

### <span data-ttu-id="20b25-126">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="20b25-126">-InformationVariable</span></span>
<span data-ttu-id="20b25-127">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="20b25-127">Specifies an information variable.</span></span>

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

### <span data-ttu-id="20b25-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="20b25-128">-Name</span></span>
<span data-ttu-id="20b25-129">指定來源虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="20b25-129">Specifies the name of the source virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20b25-130">-OSState</span><span class="sxs-lookup"><span data-stu-id="20b25-130">-OSState</span></span>
<span data-ttu-id="20b25-131">指定虛擬機器影像的作業系統狀態。</span><span class="sxs-lookup"><span data-stu-id="20b25-131">Specifies the operation system state for the virtual machine image.</span></span>
<span data-ttu-id="20b25-132">如果您想要將虛擬機器影像捕獲至 Azure，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="20b25-132">Use this parameter if you intend to capture a virtual machine image to Azure.</span></span>

<span data-ttu-id="20b25-133">有效值為：</span><span class="sxs-lookup"><span data-stu-id="20b25-133">Valid values are:</span></span>

- <span data-ttu-id="20b25-134">普通</span><span class="sxs-lookup"><span data-stu-id="20b25-134">Generalized</span></span>
- <span data-ttu-id="20b25-135">特殊化</span><span class="sxs-lookup"><span data-stu-id="20b25-135">Specialized</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20b25-136">-設定檔</span><span class="sxs-lookup"><span data-stu-id="20b25-136">-Profile</span></span>
<span data-ttu-id="20b25-137">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="20b25-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="20b25-138">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="20b25-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="20b25-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="20b25-139">-ServiceName</span></span>
<span data-ttu-id="20b25-140">指定 Azure 服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="20b25-140">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="20b25-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20b25-141">CommonParameters</span></span>
<span data-ttu-id="20b25-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="20b25-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20b25-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="20b25-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20b25-144">輸入</span><span class="sxs-lookup"><span data-stu-id="20b25-144">INPUTS</span></span>

## <span data-ttu-id="20b25-145">輸出</span><span class="sxs-lookup"><span data-stu-id="20b25-145">OUTPUTS</span></span>

## <span data-ttu-id="20b25-146">筆記</span><span class="sxs-lookup"><span data-stu-id="20b25-146">NOTES</span></span>

## <span data-ttu-id="20b25-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="20b25-147">RELATED LINKS</span></span>

[<span data-ttu-id="20b25-148">附加 AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="20b25-148">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="20b25-149">AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="20b25-149">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="20b25-150">移除-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="20b25-150">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="20b25-151">更新-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="20b25-151">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


