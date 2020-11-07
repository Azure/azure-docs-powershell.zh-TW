---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5BEE9430-D6BF-49F1-A23D-32784C6C818E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 98b9abe6bcb9998067fe978a5f99f5d8b64cd26d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967777"
---
# <span data-ttu-id="c5ccb-101">Get-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="c5ccb-101">Get-AzurePublicIP</span></span>

## <span data-ttu-id="c5ccb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c5ccb-102">SYNOPSIS</span></span>
<span data-ttu-id="c5ccb-103">取得 Azure 虛擬機器的公用 IP 資訊。</span><span class="sxs-lookup"><span data-stu-id="c5ccb-103">Gets the Public IP information for an Azure virtual machine.</span></span>

## <span data-ttu-id="c5ccb-104">句法</span><span class="sxs-lookup"><span data-stu-id="c5ccb-104">SYNTAX</span></span>

```
Get-AzurePublicIP [[-PublicIPName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c5ccb-105">說明</span><span class="sxs-lookup"><span data-stu-id="c5ccb-105">DESCRIPTION</span></span>
<span data-ttu-id="c5ccb-106">**AzurePublicIP** Cmdlet 會取得 Azure 虛擬機器的公用 IP 資訊。</span><span class="sxs-lookup"><span data-stu-id="c5ccb-106">The **Get-AzurePublicIP** cmdlet gets the Public IP information for an Azure virtual machine.</span></span>
<span data-ttu-id="c5ccb-107">若要取得公用 IP 的 IP 位址，請使用 **add-azurevm** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c5ccb-107">To obtain the IP address of the Public IP, use the **Get-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="c5ccb-108">示例</span><span class="sxs-lookup"><span data-stu-id="c5ccb-108">EXAMPLES</span></span>

### <span data-ttu-id="c5ccb-109">範例1：取得公用 IP 配置</span><span class="sxs-lookup"><span data-stu-id="c5ccb-109">Example 1: Get Public IP configuration</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Get-AzurePublicIP
```

<span data-ttu-id="c5ccb-110">這個命令會透過使用 **FTPInstance Cmdlet，** 在名為 FTPInAzure 的服務中，取得名為的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c5ccb-110">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="c5ccb-111">命令會使用管線運算子，將該虛擬機器傳至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c5ccb-111">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c5ccb-112">目前的 Cmdlet 會從虛擬機器取得公用 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="c5ccb-112">The current cmdlet gets Public IP configuration from the virtual machine.</span></span>

## <span data-ttu-id="c5ccb-113">參數</span><span class="sxs-lookup"><span data-stu-id="c5ccb-113">PARAMETERS</span></span>

### <span data-ttu-id="c5ccb-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c5ccb-114">-InformationAction</span></span>
<span data-ttu-id="c5ccb-115">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="c5ccb-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c5ccb-116">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c5ccb-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c5ccb-117">持續</span><span class="sxs-lookup"><span data-stu-id="c5ccb-117">Continue</span></span>
- <span data-ttu-id="c5ccb-118">理會</span><span class="sxs-lookup"><span data-stu-id="c5ccb-118">Ignore</span></span>
- <span data-ttu-id="c5ccb-119">看</span><span class="sxs-lookup"><span data-stu-id="c5ccb-119">Inquire</span></span>
- <span data-ttu-id="c5ccb-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c5ccb-120">SilentlyContinue</span></span>
- <span data-ttu-id="c5ccb-121">停止</span><span class="sxs-lookup"><span data-stu-id="c5ccb-121">Stop</span></span>
- <span data-ttu-id="c5ccb-122">封存</span><span class="sxs-lookup"><span data-stu-id="c5ccb-122">Suspend</span></span>

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

### <span data-ttu-id="c5ccb-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c5ccb-123">-InformationVariable</span></span>
<span data-ttu-id="c5ccb-124">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="c5ccb-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c5ccb-125">-設定檔</span><span class="sxs-lookup"><span data-stu-id="c5ccb-125">-Profile</span></span>
<span data-ttu-id="c5ccb-126">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="c5ccb-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c5ccb-127">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="c5ccb-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c5ccb-128">-PublicIPName</span><span class="sxs-lookup"><span data-stu-id="c5ccb-128">-PublicIPName</span></span>
<span data-ttu-id="c5ccb-129">指定公用 IP 名稱。</span><span class="sxs-lookup"><span data-stu-id="c5ccb-129">Specifies the Public IP name.</span></span>

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

### <span data-ttu-id="c5ccb-130">-VM</span><span class="sxs-lookup"><span data-stu-id="c5ccb-130">-VM</span></span>
<span data-ttu-id="c5ccb-131">指定此 Cmdlet 取得公用 IP 配置的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c5ccb-131">Specifies the virtual machine for which this cmdlet gets Public IP configuration.</span></span>

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

### <span data-ttu-id="c5ccb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5ccb-132">CommonParameters</span></span>
<span data-ttu-id="c5ccb-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c5ccb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5ccb-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c5ccb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5ccb-135">輸入</span><span class="sxs-lookup"><span data-stu-id="c5ccb-135">INPUTS</span></span>

## <span data-ttu-id="c5ccb-136">輸出</span><span class="sxs-lookup"><span data-stu-id="c5ccb-136">OUTPUTS</span></span>

### <span data-ttu-id="c5ccb-137">WindowsAzure ServiceManagement. AssignPublicIPCollection</span><span class="sxs-lookup"><span data-stu-id="c5ccb-137">Microsoft.WindowsAzure.Commands.ServiceManagement.AssignPublicIPCollection</span></span>

## <span data-ttu-id="c5ccb-138">筆記</span><span class="sxs-lookup"><span data-stu-id="c5ccb-138">NOTES</span></span>

## <span data-ttu-id="c5ccb-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="c5ccb-139">RELATED LINKS</span></span>

[<span data-ttu-id="c5ccb-140">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="c5ccb-140">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="c5ccb-141">移除-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="c5ccb-141">Remove-AzurePublicIP</span></span>](./Remove-AzurePublicIP.md)

[<span data-ttu-id="c5ccb-142">Set-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="c5ccb-142">Set-AzurePublicIP</span></span>](./Set-AzurePublicIP.md)


