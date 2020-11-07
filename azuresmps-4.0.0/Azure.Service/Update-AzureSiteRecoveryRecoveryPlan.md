---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 5625ED47-BD85-4BF5-9044-2012E5A67BA4
online version: ''
schema: 2.0.0
ms.openlocfilehash: d1c680adf1d9d850f89cb81e1525a0e0e06eb6c9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967460"
---
# <span data-ttu-id="3bdb5-101">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3bdb5-101">Update-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="3bdb5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3bdb5-102">SYNOPSIS</span></span>
<span data-ttu-id="3bdb5-103">在網站復原中更新復原方案。</span><span class="sxs-lookup"><span data-stu-id="3bdb5-103">Updates a recovery plan in Site Recovery.</span></span>

## <span data-ttu-id="3bdb5-104">句法</span><span class="sxs-lookup"><span data-stu-id="3bdb5-104">SYNTAX</span></span>

```
Update-AzureSiteRecoveryRecoveryPlan -File <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="3bdb5-105">說明</span><span class="sxs-lookup"><span data-stu-id="3bdb5-105">DESCRIPTION</span></span>
<span data-ttu-id="3bdb5-106">**AzureSiteRecoveryRecoveryPlan** Cmdlet 會在 Azure Site recovery 中更新復原方案，然後發佈該恢復計畫。</span><span class="sxs-lookup"><span data-stu-id="3bdb5-106">The **Update-AzureSiteRecoveryRecoveryPlan** cmdlet updates a recovery plan in Azure Site Recovery and then publishes it.</span></span>

## <span data-ttu-id="3bdb5-107">示例</span><span class="sxs-lookup"><span data-stu-id="3bdb5-107">EXAMPLES</span></span>

### <span data-ttu-id="3bdb5-108">範例1：更新復原方案</span><span class="sxs-lookup"><span data-stu-id="3bdb5-108">Example 1: Update a recovery plan</span></span>
```
PS C:\> Update-AzureSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="3bdb5-109">這個命令會更新指定的復原方案，然後發佈。</span><span class="sxs-lookup"><span data-stu-id="3bdb5-109">This command updates the specified recovery plan, and then publishes it.</span></span>

## <span data-ttu-id="3bdb5-110">參數</span><span class="sxs-lookup"><span data-stu-id="3bdb5-110">PARAMETERS</span></span>

### <span data-ttu-id="3bdb5-111">檔案</span><span class="sxs-lookup"><span data-stu-id="3bdb5-111">-File</span></span>
<span data-ttu-id="3bdb5-112">指定此 Cmdlet 更新之復原方案的恢復計畫檔案。</span><span class="sxs-lookup"><span data-stu-id="3bdb5-112">Specifies the recovery plan file of the recovery plan that this cmdlet updates.</span></span>

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

### <span data-ttu-id="3bdb5-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="3bdb5-113">-Profile</span></span>
<span data-ttu-id="3bdb5-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="3bdb5-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3bdb5-115">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="3bdb5-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3bdb5-116">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="3bdb5-116">-WaitForCompletion</span></span>
<span data-ttu-id="3bdb5-117">表示 Cmdlet 在將控制權傳回給 Windows PowerShell 主控台之前，先等待該作業完成。</span><span class="sxs-lookup"><span data-stu-id="3bdb5-117">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="3bdb5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bdb5-118">CommonParameters</span></span>
<span data-ttu-id="3bdb5-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3bdb5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bdb5-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3bdb5-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bdb5-121">輸入</span><span class="sxs-lookup"><span data-stu-id="3bdb5-121">INPUTS</span></span>

## <span data-ttu-id="3bdb5-122">輸出</span><span class="sxs-lookup"><span data-stu-id="3bdb5-122">OUTPUTS</span></span>

## <span data-ttu-id="3bdb5-123">筆記</span><span class="sxs-lookup"><span data-stu-id="3bdb5-123">NOTES</span></span>

## <span data-ttu-id="3bdb5-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="3bdb5-124">RELATED LINKS</span></span>

[<span data-ttu-id="3bdb5-125">AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3bdb5-125">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="3bdb5-126">新-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3bdb5-126">New-AzureSiteRecoveryRecoveryPlan</span></span>](./New-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="3bdb5-127">移除-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3bdb5-127">Remove-AzureSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureSiteRecoveryRecoveryPlan.md)


