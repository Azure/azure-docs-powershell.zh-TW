---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 30D56D40-2EA0-48D1-846A-AFB4A987E08F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9dac9858a251e0390fd2a11a2c01dddede1613b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967200"
---
# <span data-ttu-id="262ea-101">Set-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="262ea-101">Set-AzureSiteRecoveryVM</span></span>

## <span data-ttu-id="262ea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="262ea-102">SYNOPSIS</span></span>
<span data-ttu-id="262ea-103">設定網站恢復保護實體的復原端選項。</span><span class="sxs-lookup"><span data-stu-id="262ea-103">Sets the recovery-side options for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="262ea-104">句法</span><span class="sxs-lookup"><span data-stu-id="262ea-104">SYNTAX</span></span>

```
Set-AzureSiteRecoveryVM -VirtualMachine <ASRVirtualMachine> [-Name <String>] [-Size <String>]
 [-PrimaryNic <String>] [-RecoveryNetworkId <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="262ea-105">說明</span><span class="sxs-lookup"><span data-stu-id="262ea-105">DESCRIPTION</span></span>
<span data-ttu-id="262ea-106">**AzureSiteRecoveryVM** Cmdlet 會針對 Azure Site recovery 保護實體設定復原端保護選項，例如，恢復虛擬機器大小與復原虛擬機器網路。</span><span class="sxs-lookup"><span data-stu-id="262ea-106">The **Set-AzureSiteRecoveryVM** cmdlet sets the recovery-side protection options, such as the recovery virtual machine size and recovery virtual machine network, for Azure Site Recovery protection entities.</span></span>

## <span data-ttu-id="262ea-107">示例</span><span class="sxs-lookup"><span data-stu-id="262ea-107">EXAMPLES</span></span>

### <span data-ttu-id="262ea-108">範例1：允許更新受保護的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="262ea-108">Example 1: Allow the update on a protected virtual machine</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $VirtualMachines = Get-AzureSiteRecoveryVM -ProtectionContainer $ProtectionContainer 
PS C:\> Set-AzureSiteRecoveryVM -VirtualMachine $VirtualMachines[0] -Name "NewVirtualMachine05"
Name             : 
ID               : 8170d274-1e48-404a-b080-172ada140bc3
ClientRequestId  : 09354052-8430-4fa8-9a35-63196dd4b2b4-2015-02-03 04:19:06Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="262ea-109">第一個命令使用 **AzureSiteRecoveryProtectionContainer** Cmdlet 來取得受保護的容器，然後將它儲存在 $ProtectionContainer 變數中。</span><span class="sxs-lookup"><span data-stu-id="262ea-109">The first command uses the **Get-AzureSiteRecoveryProtectionContainer** cmdlet to get a protected container, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="262ea-110">第二個命令會使用 **AzureSiteRecoveryVM** Cmdlet，在 $ProtectionContainer 中取得虛擬機器，然後將它們儲存在 $VitrualMachines 變數中。</span><span class="sxs-lookup"><span data-stu-id="262ea-110">The second command gets the virtual machines in $ProtectionContainer, by using the **Get-AzureSiteRecoveryVM** cmdlet, and then stores them in the $VitrualMachines variable.</span></span>

<span data-ttu-id="262ea-111">最後一個命令可允許 $VitrualMachines 陣列（名為 NewVirtualMachine05）中的第一個虛擬機器進行更新。</span><span class="sxs-lookup"><span data-stu-id="262ea-111">The final command allows updates for the first virtual machine in the $VitrualMachines array, named NewVirtualMachine05.</span></span>

## <span data-ttu-id="262ea-112">參數</span><span class="sxs-lookup"><span data-stu-id="262ea-112">PARAMETERS</span></span>

### <span data-ttu-id="262ea-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="262ea-113">-Name</span></span>
<span data-ttu-id="262ea-114">指定目標虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="262ea-114">Specifies the name of the target virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="262ea-115">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="262ea-115">-PrimaryNic</span></span>
<span data-ttu-id="262ea-116">指定主要網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="262ea-116">Specifies the primary network adapter card.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="262ea-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="262ea-117">-Profile</span></span>
<span data-ttu-id="262ea-118">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="262ea-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="262ea-119">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="262ea-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="262ea-120">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="262ea-120">-RecoveryNetworkId</span></span>
<span data-ttu-id="262ea-121">指定恢復網路識別碼。</span><span class="sxs-lookup"><span data-stu-id="262ea-121">Specifies the recovery network ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="262ea-122">-大小</span><span class="sxs-lookup"><span data-stu-id="262ea-122">-Size</span></span>
<span data-ttu-id="262ea-123">指定目標虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="262ea-123">Specifies the target virtual machine size.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="262ea-124">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="262ea-124">-VirtualMachine</span></span>
<span data-ttu-id="262ea-125">指定網站復原虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="262ea-125">Specifies the Site Recovery virtual machine object.</span></span>

```yaml
Type: ASRVirtualMachine
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="262ea-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="262ea-126">CommonParameters</span></span>
<span data-ttu-id="262ea-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="262ea-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="262ea-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="262ea-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="262ea-129">輸入</span><span class="sxs-lookup"><span data-stu-id="262ea-129">INPUTS</span></span>

## <span data-ttu-id="262ea-130">輸出</span><span class="sxs-lookup"><span data-stu-id="262ea-130">OUTPUTS</span></span>

## <span data-ttu-id="262ea-131">筆記</span><span class="sxs-lookup"><span data-stu-id="262ea-131">NOTES</span></span>

## <span data-ttu-id="262ea-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="262ea-132">RELATED LINKS</span></span>

[<span data-ttu-id="262ea-133">AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="262ea-133">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="262ea-134">AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="262ea-134">Get-AzureSiteRecoveryVM</span></span>](./Get-AzureSiteRecoveryVM.md)


