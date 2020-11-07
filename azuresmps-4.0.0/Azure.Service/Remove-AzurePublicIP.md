---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9EA98944-1923-4573-991E-3B9CA21004BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f16b51dc8abf5c6243b4b489789d65029acc3c4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967594"
---
# <span data-ttu-id="7430f-101">Remove-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="7430f-101">Remove-AzurePublicIP</span></span>

## <span data-ttu-id="7430f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7430f-102">SYNOPSIS</span></span>
<span data-ttu-id="7430f-103">從 Azure 虛擬機器移除公用 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="7430f-103">Removes Public IP configuration from an Azure virtual machine.</span></span>

## <span data-ttu-id="7430f-104">句法</span><span class="sxs-lookup"><span data-stu-id="7430f-104">SYNTAX</span></span>

```
Remove-AzurePublicIP [[-PublicIPName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7430f-105">說明</span><span class="sxs-lookup"><span data-stu-id="7430f-105">DESCRIPTION</span></span>
<span data-ttu-id="7430f-106">**AzurePublicIP** Cmdlet 會從 Azure 虛擬機器中移除公用 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="7430f-106">The **Remove-AzurePublicIP** cmdlet removes Public IP configuration from an Azure virtual machine.</span></span>

## <span data-ttu-id="7430f-107">示例</span><span class="sxs-lookup"><span data-stu-id="7430f-107">EXAMPLES</span></span>

### <span data-ttu-id="7430f-108">範例1：移除公用 IP 設定</span><span class="sxs-lookup"><span data-stu-id="7430f-108">Example 1: Remove Public IP configuration</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Remove-AzurePublicIP | Update-AzureVM
```

<span data-ttu-id="7430f-109">這個命令會透過使用 **FTPInstance Cmdlet，** 在名為 FTPInAzure 的服務中，取得名為的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="7430f-109">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="7430f-110">命令會使用管線運算子，將該虛擬機器傳至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7430f-110">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7430f-111">目前的 Cmdlet 會從虛擬機器中移除公用 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="7430f-111">The current cmdlet removes Public IP configuration from the virtual machine.</span></span>
<span data-ttu-id="7430f-112">該命令會將虛擬機器傳到由 **add-azurevm** Cmdlet （可實現您的變更）。</span><span class="sxs-lookup"><span data-stu-id="7430f-112">The command passes the virtual machine to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

## <span data-ttu-id="7430f-113">參數</span><span class="sxs-lookup"><span data-stu-id="7430f-113">PARAMETERS</span></span>

### <span data-ttu-id="7430f-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7430f-114">-InformationAction</span></span>
<span data-ttu-id="7430f-115">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="7430f-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7430f-116">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="7430f-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7430f-117">持續</span><span class="sxs-lookup"><span data-stu-id="7430f-117">Continue</span></span>
- <span data-ttu-id="7430f-118">理會</span><span class="sxs-lookup"><span data-stu-id="7430f-118">Ignore</span></span>
- <span data-ttu-id="7430f-119">看</span><span class="sxs-lookup"><span data-stu-id="7430f-119">Inquire</span></span>
- <span data-ttu-id="7430f-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7430f-120">SilentlyContinue</span></span>
- <span data-ttu-id="7430f-121">停止</span><span class="sxs-lookup"><span data-stu-id="7430f-121">Stop</span></span>
- <span data-ttu-id="7430f-122">封存</span><span class="sxs-lookup"><span data-stu-id="7430f-122">Suspend</span></span>

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

### <span data-ttu-id="7430f-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7430f-123">-InformationVariable</span></span>
<span data-ttu-id="7430f-124">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="7430f-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7430f-125">-設定檔</span><span class="sxs-lookup"><span data-stu-id="7430f-125">-Profile</span></span>
<span data-ttu-id="7430f-126">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="7430f-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7430f-127">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="7430f-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7430f-128">-PublicIPName</span><span class="sxs-lookup"><span data-stu-id="7430f-128">-PublicIPName</span></span>
<span data-ttu-id="7430f-129">指定公用 IP 名稱。</span><span class="sxs-lookup"><span data-stu-id="7430f-129">Specifies the Public IP name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7430f-130">-VM</span><span class="sxs-lookup"><span data-stu-id="7430f-130">-VM</span></span>
<span data-ttu-id="7430f-131">指定此 Cmdlet 移除公用 IP 配置的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="7430f-131">Specifies the virtual machine from which this cmdlet removes Public IP configuration.</span></span>

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

### <span data-ttu-id="7430f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7430f-132">CommonParameters</span></span>
<span data-ttu-id="7430f-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7430f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7430f-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7430f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7430f-135">輸入</span><span class="sxs-lookup"><span data-stu-id="7430f-135">INPUTS</span></span>

## <span data-ttu-id="7430f-136">輸出</span><span class="sxs-lookup"><span data-stu-id="7430f-136">OUTPUTS</span></span>

### <span data-ttu-id="7430f-137">WindowsAzure. ServiceManagement. IPersistentVM</span><span class="sxs-lookup"><span data-stu-id="7430f-137">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.IPersistentVM</span></span>

## <span data-ttu-id="7430f-138">筆記</span><span class="sxs-lookup"><span data-stu-id="7430f-138">NOTES</span></span>

## <span data-ttu-id="7430f-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="7430f-139">RELATED LINKS</span></span>

[<span data-ttu-id="7430f-140">AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="7430f-140">Get-AzurePublicIP</span></span>](./Get-AzurePublicIP.md)

[<span data-ttu-id="7430f-141">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="7430f-141">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="7430f-142">Set-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="7430f-142">Set-AzurePublicIP</span></span>](./Set-AzurePublicIP.md)

[<span data-ttu-id="7430f-143">更新-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="7430f-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


