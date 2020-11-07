---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8A6B2633-EECC-416A-85F6-69C8341AA970
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82ef50dcdf5f17e044a9dc2091cbfda5cb5d1b2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967066"
---
# <span data-ttu-id="460b7-101">Get-AzureRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="460b7-101">Get-AzureRemoteDesktopFile</span></span>

## <span data-ttu-id="460b7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="460b7-102">SYNOPSIS</span></span>
<span data-ttu-id="460b7-103">取得 Azure 虛擬機器的 RDP 檔案。</span><span class="sxs-lookup"><span data-stu-id="460b7-103">Gets an RDP file for an Azure virtual machine.</span></span>

## <span data-ttu-id="460b7-104">句法</span><span class="sxs-lookup"><span data-stu-id="460b7-104">SYNTAX</span></span>

### <span data-ttu-id="460b7-105">下載 (預設) </span><span class="sxs-lookup"><span data-stu-id="460b7-105">Download (Default)</span></span>
```
Get-AzureRemoteDesktopFile [-Name] <String> [-LocalPath] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="460b7-106">發起</span><span class="sxs-lookup"><span data-stu-id="460b7-106">Launch</span></span>
```
Get-AzureRemoteDesktopFile [-Name] <String> [[-LocalPath] <String>] [-Launch] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="460b7-107">說明</span><span class="sxs-lookup"><span data-stu-id="460b7-107">DESCRIPTION</span></span>
<span data-ttu-id="460b7-108">**AzureRemoteDesktopFile** Cmdlet 會針對 Azure 虛擬機器下載並儲存遠端桌面連線 (RDP) 檔案。</span><span class="sxs-lookup"><span data-stu-id="460b7-108">The **Get-AzureRemoteDesktopFile** cmdlet downloads and saves a remote desktop connection (RDP) file for an Azure virtual machine.</span></span>
<span data-ttu-id="460b7-109">這個 Cmdlet 可以啟動遠端桌面連線至指定的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="460b7-109">The cmdlet can launch a remote desktop connection to the specified virtual machine.</span></span>

## <span data-ttu-id="460b7-110">示例</span><span class="sxs-lookup"><span data-stu-id="460b7-110">EXAMPLES</span></span>

### <span data-ttu-id="460b7-111">範例1：取得 RDP 檔案</span><span class="sxs-lookup"><span data-stu-id="460b7-111">Example 1: Get an RDP file</span></span>
```
PS C:\> Get-AzureRemoteDesktopFile -ServiceName "ContosoService" -Name "VirtualMachine07" -LocalPath "C:\temp\VirtualMachine07.rdp"
```

<span data-ttu-id="460b7-112">這個命令會取得名為 VirtualMachine07 的 VirtualMachine07 虛擬機器的 RDP 檔案，該檔案是在名為 ContosoService 的服務上執行。</span><span class="sxs-lookup"><span data-stu-id="460b7-112">This command gets an RDP file for the VirtualMachine07 virtual machine named VirtualMachine07 that runs on the service named ContosoService.</span></span>
<span data-ttu-id="460b7-113">該命令會將該檔案儲存為 C:\temp\VirtualMachine07.rdp。</span><span class="sxs-lookup"><span data-stu-id="460b7-113">The command stores that file as C:\temp\VirtualMachine07.rdp.</span></span>

### <span data-ttu-id="460b7-114">範例2：啟動遠端會話</span><span class="sxs-lookup"><span data-stu-id="460b7-114">Example 2: Start a remote session</span></span>
```
PS C:\> Get-AzureRemoteDesktopFile -ServiceName "ContosoService" -Name "VirtualMachine07" -Launch
```

<span data-ttu-id="460b7-115">這個命令會取得名為 VirtualMachine07 的 VirtualMachine07 虛擬機器的 RDP 檔案，該檔案是在名為 ContosoService 的服務上執行。</span><span class="sxs-lookup"><span data-stu-id="460b7-115">This command gets an RDP file for the VirtualMachine07 virtual machine named VirtualMachine07 that runs on the service named ContosoService.</span></span>
<span data-ttu-id="460b7-116">命令會啟動遠端桌面會話。</span><span class="sxs-lookup"><span data-stu-id="460b7-116">The command launches a remote desktop session.</span></span>
<span data-ttu-id="460b7-117">關閉連線時，該命令會刪除 RDP 檔案。</span><span class="sxs-lookup"><span data-stu-id="460b7-117">The command deletes the RDP file when the connection is closed.</span></span>

## <span data-ttu-id="460b7-118">參數</span><span class="sxs-lookup"><span data-stu-id="460b7-118">PARAMETERS</span></span>

### <span data-ttu-id="460b7-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="460b7-119">-InformationAction</span></span>
<span data-ttu-id="460b7-120">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="460b7-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="460b7-121">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="460b7-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="460b7-122">持續</span><span class="sxs-lookup"><span data-stu-id="460b7-122">Continue</span></span>
- <span data-ttu-id="460b7-123">理會</span><span class="sxs-lookup"><span data-stu-id="460b7-123">Ignore</span></span>
- <span data-ttu-id="460b7-124">看</span><span class="sxs-lookup"><span data-stu-id="460b7-124">Inquire</span></span>
- <span data-ttu-id="460b7-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="460b7-125">SilentlyContinue</span></span>
- <span data-ttu-id="460b7-126">停止</span><span class="sxs-lookup"><span data-stu-id="460b7-126">Stop</span></span>
- <span data-ttu-id="460b7-127">封存</span><span class="sxs-lookup"><span data-stu-id="460b7-127">Suspend</span></span>

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

### <span data-ttu-id="460b7-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="460b7-128">-InformationVariable</span></span>
<span data-ttu-id="460b7-129">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="460b7-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="460b7-130">-啟動</span><span class="sxs-lookup"><span data-stu-id="460b7-130">-Launch</span></span>
<span data-ttu-id="460b7-131">表示此 Cmdlet 會啟動遠端桌面會話至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="460b7-131">Indicates that this cmdlet starts a remote desktop session to the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Launch
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="460b7-132">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="460b7-132">-LocalPath</span></span>
<span data-ttu-id="460b7-133">指定本機電腦上已下載 RDP 檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="460b7-133">Specifies the full path of the downloaded RDP file on the local computer.</span></span>

```yaml
Type: String
Parameter Sets: Download
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Launch
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="460b7-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="460b7-134">-Name</span></span>
<span data-ttu-id="460b7-135">指定此 Cmdlet 下載 RDP 檔案的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="460b7-135">Specifies the virtual machine for which this cmdlet downloads an RDP file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="460b7-136">-設定檔</span><span class="sxs-lookup"><span data-stu-id="460b7-136">-Profile</span></span>
<span data-ttu-id="460b7-137">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="460b7-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="460b7-138">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="460b7-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="460b7-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="460b7-139">-ServiceName</span></span>
<span data-ttu-id="460b7-140">指定虛擬機器所屬之 Azure 服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="460b7-140">Specifies the name of the Azure service to which the virtual machine belongs.</span></span>

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

### <span data-ttu-id="460b7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="460b7-141">CommonParameters</span></span>
<span data-ttu-id="460b7-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="460b7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="460b7-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="460b7-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="460b7-144">輸入</span><span class="sxs-lookup"><span data-stu-id="460b7-144">INPUTS</span></span>

## <span data-ttu-id="460b7-145">輸出</span><span class="sxs-lookup"><span data-stu-id="460b7-145">OUTPUTS</span></span>

## <span data-ttu-id="460b7-146">筆記</span><span class="sxs-lookup"><span data-stu-id="460b7-146">NOTES</span></span>

## <span data-ttu-id="460b7-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="460b7-147">RELATED LINKS</span></span>

