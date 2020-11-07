---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 8557B04E-DE35-473E-8F5D-B72B70300AA6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1949d30d6bbea16e1626954bf241df36d81533e1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967031"
---
# <span data-ttu-id="60c48-101">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="60c48-101">Get-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="60c48-102">摘要</span><span class="sxs-lookup"><span data-stu-id="60c48-102">SYNOPSIS</span></span>
<span data-ttu-id="60c48-103">在網站復原中取得復原計畫。</span><span class="sxs-lookup"><span data-stu-id="60c48-103">Gets a recovery plan in Site Recovery.</span></span>

## <span data-ttu-id="60c48-104">句法</span><span class="sxs-lookup"><span data-stu-id="60c48-104">SYNTAX</span></span>

### <span data-ttu-id="60c48-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="60c48-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="60c48-106">ById</span><span class="sxs-lookup"><span data-stu-id="60c48-106">ById</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="60c48-107">ByName</span><span class="sxs-lookup"><span data-stu-id="60c48-107">ByName</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="60c48-108">說明</span><span class="sxs-lookup"><span data-stu-id="60c48-108">DESCRIPTION</span></span>
<span data-ttu-id="60c48-109">**AzureSiteRecoveryRecoveryPlan** Cmdlet 會在 Azure Site recovery 中取得恢復方案。</span><span class="sxs-lookup"><span data-stu-id="60c48-109">The **Get-AzureSiteRecoveryRecoveryPlan** cmdlet gets a recovery plan in Azure Site Recovery.</span></span>

## <span data-ttu-id="60c48-110">示例</span><span class="sxs-lookup"><span data-stu-id="60c48-110">EXAMPLES</span></span>

### <span data-ttu-id="60c48-111">範例1：取得恢復計畫</span><span class="sxs-lookup"><span data-stu-id="60c48-111">Example 1: Get a recovery plan</span></span>
```
PS C:\> Get-AzureSiteRecoveryRecoveryPlan
ID                            Name                          ServerId                      TargetServerId
--                            ----                          --------                      --------------
71de8ebc-1e9a-4242-aec3-ee... ContosoPlan                   4a94c4a9-c856-4577-afbd-36... 78facf56-b273-4941-82fd-cc...
```

<span data-ttu-id="60c48-112">這個命令會取得目前 Azure Site Recovery 保存庫的復原方案資訊。</span><span class="sxs-lookup"><span data-stu-id="60c48-112">This command gets information about the recovery plan for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="60c48-113">參數</span><span class="sxs-lookup"><span data-stu-id="60c48-113">PARAMETERS</span></span>

### <span data-ttu-id="60c48-114">-識別碼</span><span class="sxs-lookup"><span data-stu-id="60c48-114">-Id</span></span>
<span data-ttu-id="60c48-115">指定要取得的復原方案 ID。</span><span class="sxs-lookup"><span data-stu-id="60c48-115">Specifies the ID of the recovery plan to get.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c48-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="60c48-116">-Name</span></span>
<span data-ttu-id="60c48-117">指定要取得的復原方案名稱。</span><span class="sxs-lookup"><span data-stu-id="60c48-117">Specifies the name of the recovery plan to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c48-118">-設定檔</span><span class="sxs-lookup"><span data-stu-id="60c48-118">-Profile</span></span>
<span data-ttu-id="60c48-119">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="60c48-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="60c48-120">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="60c48-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="60c48-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60c48-121">CommonParameters</span></span>
<span data-ttu-id="60c48-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="60c48-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60c48-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="60c48-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60c48-124">輸入</span><span class="sxs-lookup"><span data-stu-id="60c48-124">INPUTS</span></span>

## <span data-ttu-id="60c48-125">輸出</span><span class="sxs-lookup"><span data-stu-id="60c48-125">OUTPUTS</span></span>

## <span data-ttu-id="60c48-126">筆記</span><span class="sxs-lookup"><span data-stu-id="60c48-126">NOTES</span></span>

## <span data-ttu-id="60c48-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="60c48-127">RELATED LINKS</span></span>

[<span data-ttu-id="60c48-128">新-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="60c48-128">New-AzureSiteRecoveryRecoveryPlan</span></span>](./New-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="60c48-129">移除-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="60c48-129">Remove-AzureSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="60c48-130">更新-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="60c48-130">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)


