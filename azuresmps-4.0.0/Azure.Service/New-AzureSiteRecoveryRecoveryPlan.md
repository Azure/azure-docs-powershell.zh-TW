---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2F749E4A-149F-44E0-8AEB-F2C416140906
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7d1162ed2c9126942cc6ae31cbe31fdc2ef130d8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967422"
---
# <span data-ttu-id="5d887-101">New-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5d887-101">New-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="5d887-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5d887-102">SYNOPSIS</span></span>
<span data-ttu-id="5d887-103">在網站還原中建立網站復原方案。</span><span class="sxs-lookup"><span data-stu-id="5d887-103">Creates a site recovery plan in Site Recovery.</span></span>

## <span data-ttu-id="5d887-104">句法</span><span class="sxs-lookup"><span data-stu-id="5d887-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryRecoveryPlan -File <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d887-105">說明</span><span class="sxs-lookup"><span data-stu-id="5d887-105">DESCRIPTION</span></span>
<span data-ttu-id="5d887-106">**新的-AzureSiteRecoveryRecoveryPlan** Cmdlet 會在 Azure Site recovery 中建立恢復方案。</span><span class="sxs-lookup"><span data-stu-id="5d887-106">The **New-AzureSiteRecoveryRecoveryPlan** cmdlet creates a recovery plan in Azure Site Recovery.</span></span>

<span data-ttu-id="5d887-107">針對容錯移轉與復原的目的，復原方案會收集群組中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5d887-107">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="5d887-108">示例</span><span class="sxs-lookup"><span data-stu-id="5d887-108">EXAMPLES</span></span>

### <span data-ttu-id="5d887-109">範例1：將復原方案新增至網站復原電子倉庫</span><span class="sxs-lookup"><span data-stu-id="5d887-109">Example 1: Add a recovery plan to a Site Recovery vault</span></span>
```
PS C:\> New-AzureSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="5d887-110">這個命令會將名為 RecoveryPlan.xml 的復原方案新增至 Azure Site Recovery 保存庫。</span><span class="sxs-lookup"><span data-stu-id="5d887-110">This command adds the recovery plan named RecoveryPlan.xml to the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="5d887-111">參數</span><span class="sxs-lookup"><span data-stu-id="5d887-111">PARAMETERS</span></span>

### <span data-ttu-id="5d887-112">檔案</span><span class="sxs-lookup"><span data-stu-id="5d887-112">-File</span></span>
<span data-ttu-id="5d887-113">指定復原方案檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="5d887-113">Specifies the path of the recovery plan file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d887-114">-設定檔</span><span class="sxs-lookup"><span data-stu-id="5d887-114">-Profile</span></span>
<span data-ttu-id="5d887-115">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="5d887-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5d887-116">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="5d887-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5d887-117">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="5d887-117">-WaitForCompletion</span></span>
<span data-ttu-id="5d887-118">表示 Cmdlet 在將控制權傳回給 Windows PowerShell 主控台之前，先等待該作業完成。</span><span class="sxs-lookup"><span data-stu-id="5d887-118">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="5d887-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d887-119">CommonParameters</span></span>
<span data-ttu-id="5d887-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5d887-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d887-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5d887-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d887-122">輸入</span><span class="sxs-lookup"><span data-stu-id="5d887-122">INPUTS</span></span>

## <span data-ttu-id="5d887-123">輸出</span><span class="sxs-lookup"><span data-stu-id="5d887-123">OUTPUTS</span></span>

## <span data-ttu-id="5d887-124">筆記</span><span class="sxs-lookup"><span data-stu-id="5d887-124">NOTES</span></span>

## <span data-ttu-id="5d887-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="5d887-125">RELATED LINKS</span></span>

[<span data-ttu-id="5d887-126">AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5d887-126">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="5d887-127">移除-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5d887-127">Remove-AzureSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="5d887-128">更新-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5d887-128">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)


