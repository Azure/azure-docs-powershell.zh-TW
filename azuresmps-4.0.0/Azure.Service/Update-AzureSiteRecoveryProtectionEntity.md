---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 16146A0D-4605-489A-8259-A37BEAC98306
online version: ''
schema: 2.0.0
ms.openlocfilehash: 664c9af9373120f293153a1bbdc65d1a82637631
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967461"
---
# <span data-ttu-id="f2cb1-101">Update-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f2cb1-101">Update-AzureSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="f2cb1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f2cb1-102">SYNOPSIS</span></span>
<span data-ttu-id="f2cb1-103">在 Azure Site Recovery 中更新保護實體的屬性。</span><span class="sxs-lookup"><span data-stu-id="f2cb1-103">Updates the properties of a protection entity in Azure Site Recovery.</span></span>

## <span data-ttu-id="f2cb1-104">句法</span><span class="sxs-lookup"><span data-stu-id="f2cb1-104">SYNTAX</span></span>

```
Update-AzureSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f2cb1-105">說明</span><span class="sxs-lookup"><span data-stu-id="f2cb1-105">DESCRIPTION</span></span>
<span data-ttu-id="f2cb1-106">**AzureSiteRecoveryProtectionEntity** Cmdlet 會更新 Azure Site Recovery （例如虛擬機器擁有者資訊）中保護實體的屬性。</span><span class="sxs-lookup"><span data-stu-id="f2cb1-106">The **Update-AzureSiteRecoveryProtectionEntity** cmdlet updates the properties of a protection entity in Azure Site Recovery, such as virtual machine owner information.</span></span>
<span data-ttu-id="f2cb1-107">只有虛擬機器監視器 (VMM) 至 VMM 受保護的保護實體，才能支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f2cb1-107">This cmdlet is supported only for Virtual Machine Monitor (VMM) to VMM protected protection entities.</span></span>

## <span data-ttu-id="f2cb1-108">示例</span><span class="sxs-lookup"><span data-stu-id="f2cb1-108">EXAMPLES</span></span>

### <span data-ttu-id="f2cb1-109">範例1：更新保護實體</span><span class="sxs-lookup"><span data-stu-id="f2cb1-109">Example 1: Update a protection entity</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container
PS C:\> Update-AzureSiteRecoveryProtectionEntity -ProtectionEntity $ProtectionEntity
           Name             : 
           ID               : 680ffe0f-6236-465e-8c94-81242fa67e6d
           ClientRequestId  : 2c47e6ce-1460-4187-8a0f-b9073735fa38-2014-12-30 06:44:40Z-P
           State            : NotStarted
           StateDescription : NotStarted
           StartTime        : 
           EndTime          : 
           AllowedActions   : {}
           Tasks            : {}
           Errors           : {}
```

<span data-ttu-id="f2cb1-110">第一個命令會使用 **AzureSiteRecoveryProtectionContainer** Cmdlet 取得受保護的容器，然後將該物件儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="f2cb1-110">The first command gets a protected container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that object in the $Container variable.</span></span>

<span data-ttu-id="f2cb1-111">第二個命令會使用 **AzureSiteRecoveryProtectionEntity** Cmdlet 來取得屬於儲存在 $Container 之容器的受保護虛擬機器，然後將其儲存在 $ProtectionEntity 變數中。</span><span class="sxs-lookup"><span data-stu-id="f2cb1-111">The second command gets the protected virtual machine that belongs to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet, and then stores it in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="f2cb1-112">最後一個命令會更新 $ProtectionEntity 中的保護實體。</span><span class="sxs-lookup"><span data-stu-id="f2cb1-112">The final command updates the protection entity in $ProtectionEntity.</span></span>

## <span data-ttu-id="f2cb1-113">參數</span><span class="sxs-lookup"><span data-stu-id="f2cb1-113">PARAMETERS</span></span>

### <span data-ttu-id="f2cb1-114">-設定檔</span><span class="sxs-lookup"><span data-stu-id="f2cb1-114">-Profile</span></span>
<span data-ttu-id="f2cb1-115">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="f2cb1-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f2cb1-116">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="f2cb1-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f2cb1-117">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f2cb1-117">-ProtectionEntity</span></span>
<span data-ttu-id="f2cb1-118">指定要更新的保護實體。</span><span class="sxs-lookup"><span data-stu-id="f2cb1-118">Specifies a protection entity to update.</span></span>
<span data-ttu-id="f2cb1-119">若要取得 **ASRProtectionEntity** 物件，請使用 **AzureSiteRecoveryProtectionEntity** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f2cb1-119">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2cb1-120">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="f2cb1-120">-WaitForCompletion</span></span>
<span data-ttu-id="f2cb1-121">指示這個指令在將控制權傳回給 Windows PowerShell 主控台之前，請先等待該作業完成。</span><span class="sxs-lookup"><span data-stu-id="f2cb1-121">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2cb1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2cb1-122">CommonParameters</span></span>
<span data-ttu-id="f2cb1-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f2cb1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2cb1-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f2cb1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2cb1-125">輸入</span><span class="sxs-lookup"><span data-stu-id="f2cb1-125">INPUTS</span></span>

## <span data-ttu-id="f2cb1-126">輸出</span><span class="sxs-lookup"><span data-stu-id="f2cb1-126">OUTPUTS</span></span>

## <span data-ttu-id="f2cb1-127">筆記</span><span class="sxs-lookup"><span data-stu-id="f2cb1-127">NOTES</span></span>

## <span data-ttu-id="f2cb1-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2cb1-128">RELATED LINKS</span></span>

[<span data-ttu-id="f2cb1-129">AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f2cb1-129">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="f2cb1-130">AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f2cb1-130">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="f2cb1-131">Set-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f2cb1-131">Set-AzureSiteRecoveryProtectionEntity</span></span>](./Set-AzureSiteRecoveryProtectionEntity.md)


