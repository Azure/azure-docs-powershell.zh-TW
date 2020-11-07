---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9D6D1890-9442-45F1-A3AA-BB1DB5CB33D6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 462d40e463edf6894810ac6e00e39b9c7a9eabe1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967984"
---
# <span data-ttu-id="13760-101">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="13760-101">Get-AzureVMDscExtension</span></span>

## <span data-ttu-id="13760-102">摘要</span><span class="sxs-lookup"><span data-stu-id="13760-102">SYNOPSIS</span></span>
<span data-ttu-id="13760-103">取得虛擬機器上的 DSC 延伸設定。</span><span class="sxs-lookup"><span data-stu-id="13760-103">Gets the settings of the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="13760-104">句法</span><span class="sxs-lookup"><span data-stu-id="13760-104">SYNTAX</span></span>

```
Get-AzureVMDscExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="13760-105">說明</span><span class="sxs-lookup"><span data-stu-id="13760-105">DESCRIPTION</span></span>
<span data-ttu-id="13760-106">**AzureVMDscExtension** Cmdlet 會取得虛擬機器上 DSC 延伸的設定。</span><span class="sxs-lookup"><span data-stu-id="13760-106">The **Get-AzureVMDscExtension** cmdlet gets the settings of the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="13760-107">示例</span><span class="sxs-lookup"><span data-stu-id="13760-107">EXAMPLES</span></span>

### <span data-ttu-id="13760-108">範例1：在虛擬機器上取得 DSC 延伸設定</span><span class="sxs-lookup"><span data-stu-id="13760-108">Example 1: Get the setting of the DSC Extension on a virtual machine</span></span>
```
PS C:\> Get-AzureVMDscExtension -VM $VMModulesUrl
https://myaccount.blob.core.contoso.net/windows-powershell-dsc/MyConfiguration.ps1.zipConfigurationFunction : MyConfiguration.ps1\MyConfigurationProperties            : {ServerName}ExtensionName         : DSCPublisher             : Microsoft.PowershellVersion               : 1.*PrivateConfiguration  :PublicConfiguration   : {"ModulesUrl": "https://myaccount.blob.core.contoso.net/windows-powershell-dsc/MyConfiguration.ps1.zip","ConfigurationFunction": "MyConfiguration.ps1\\MyConfiguration","Properties": {"ServerName": "C:\\MyDirectory"}}ReferenceName         : DSCState                 : EnableRoleName              : my-vm
```

<span data-ttu-id="13760-109">這個命令會取得虛擬機器上的 DSC 延伸設定。</span><span class="sxs-lookup"><span data-stu-id="13760-109">This command gets the settings of the DSC Extension on a virtual machine.</span></span>

## <span data-ttu-id="13760-110">參數</span><span class="sxs-lookup"><span data-stu-id="13760-110">PARAMETERS</span></span>

### <span data-ttu-id="13760-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="13760-111">-InformationAction</span></span>
<span data-ttu-id="13760-112">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="13760-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="13760-113">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="13760-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="13760-114">持續</span><span class="sxs-lookup"><span data-stu-id="13760-114">Continue</span></span>
- <span data-ttu-id="13760-115">理會</span><span class="sxs-lookup"><span data-stu-id="13760-115">Ignore</span></span>
- <span data-ttu-id="13760-116">看</span><span class="sxs-lookup"><span data-stu-id="13760-116">Inquire</span></span>
- <span data-ttu-id="13760-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="13760-117">SilentlyContinue</span></span>
- <span data-ttu-id="13760-118">停止</span><span class="sxs-lookup"><span data-stu-id="13760-118">Stop</span></span>
- <span data-ttu-id="13760-119">封存</span><span class="sxs-lookup"><span data-stu-id="13760-119">Suspend</span></span>

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

### <span data-ttu-id="13760-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="13760-120">-InformationVariable</span></span>
<span data-ttu-id="13760-121">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="13760-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="13760-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="13760-122">-Profile</span></span>
<span data-ttu-id="13760-123">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="13760-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="13760-124">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="13760-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="13760-125">-VM</span><span class="sxs-lookup"><span data-stu-id="13760-125">-VM</span></span>
<span data-ttu-id="13760-126">指定持久性虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="13760-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="13760-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13760-127">CommonParameters</span></span>
<span data-ttu-id="13760-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="13760-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13760-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="13760-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13760-130">輸入</span><span class="sxs-lookup"><span data-stu-id="13760-130">INPUTS</span></span>

## <span data-ttu-id="13760-131">輸出</span><span class="sxs-lookup"><span data-stu-id="13760-131">OUTPUTS</span></span>

### <span data-ttu-id="13760-132">VirtualMachineDscExtensionCoNtext WindowsAzure. ServiceManagement。</span><span class="sxs-lookup"><span data-stu-id="13760-132">Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="13760-133">筆記</span><span class="sxs-lookup"><span data-stu-id="13760-133">NOTES</span></span>

## <span data-ttu-id="13760-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="13760-134">RELATED LINKS</span></span>

[<span data-ttu-id="13760-135">移除-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="13760-135">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="13760-136">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="13760-136">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)

[<span data-ttu-id="13760-137">AzureVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="13760-137">Get-AzureVMDscExtensionStatus</span></span>](./Get-AzureVMDscExtensionStatus.md)


