---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 00B8AB6D-02E0-45B5-AB69-49FC69246A34
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb66f34cea13ac95cac47738e7cec214a6a10103
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967029"
---
# <span data-ttu-id="5b0cb-101">Get-AzureSiteRecoveryRecoveryPlanFile</span><span class="sxs-lookup"><span data-stu-id="5b0cb-101">Get-AzureSiteRecoveryRecoveryPlanFile</span></span>

## <span data-ttu-id="5b0cb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5b0cb-102">SYNOPSIS</span></span>
<span data-ttu-id="5b0cb-103">下載 XML 格式的 Azure Site Recovery 方案。</span><span class="sxs-lookup"><span data-stu-id="5b0cb-103">Downloads an Azure Site Recovery plan in XML format.</span></span>

## <span data-ttu-id="5b0cb-104">句法</span><span class="sxs-lookup"><span data-stu-id="5b0cb-104">SYNTAX</span></span>

### <span data-ttu-id="5b0cb-105">ByRPObject (預設) </span><span class="sxs-lookup"><span data-stu-id="5b0cb-105">ByRPObject (Default)</span></span>
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -RecoveryPlan <ASRRecoveryPlan>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5b0cb-106">ById</span><span class="sxs-lookup"><span data-stu-id="5b0cb-106">ById</span></span>
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -Id <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b0cb-107">說明</span><span class="sxs-lookup"><span data-stu-id="5b0cb-107">DESCRIPTION</span></span>
<span data-ttu-id="5b0cb-108">**AzureSiteRecoveryRecoveryPlanFile** Cmdlet 會以 XML 格式下載 Azure 網站復原方案。</span><span class="sxs-lookup"><span data-stu-id="5b0cb-108">The **Get-AzureSiteRecoveryRecoveryPlanFile** cmdlet downloads an Azure Site Recovery plan in XML format.</span></span>
<span data-ttu-id="5b0cb-109">您可以使用此檔案來更新復原方案，然後將它上傳到網站復原伺服器。</span><span class="sxs-lookup"><span data-stu-id="5b0cb-109">You can use this file to update the recovery plan and then upload it to the Site Recovery server.</span></span>

<span data-ttu-id="5b0cb-110">針對容錯移轉與復原的目的，復原方案會收集群組中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5b0cb-110">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="5b0cb-111">示例</span><span class="sxs-lookup"><span data-stu-id="5b0cb-111">EXAMPLES</span></span>

### <span data-ttu-id="5b0cb-112">範例1：取得恢復計畫檔案</span><span class="sxs-lookup"><span data-stu-id="5b0cb-112">Example 1: Get a recovery plan file</span></span>
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan 
PS C:\> Get-AzureSiteRecoveryRecoveryPlanFile -RecoveryPlan $RecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="5b0cb-113">這個命令會使用 **AzureSiteRecoveryRecoveryPlan** Cmdlet 來取得復原方案，然後將它儲存在 $RecoveryPlan 變數中。</span><span class="sxs-lookup"><span data-stu-id="5b0cb-113">This command uses the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet to get the recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="5b0cb-114">第二個命令使用 **GetAzureSiteRecoveryRecoveryPlanFile** Cmdlet 來取得 $RecoveryPlan 中的網站復原計畫 XML 檔案。</span><span class="sxs-lookup"><span data-stu-id="5b0cb-114">The second command uses the **GetAzureSiteRecoveryRecoveryPlanFile** cmdlet to get the site recovery plan XML file in $RecoveryPlan.</span></span>
<span data-ttu-id="5b0cb-115">該命令會將 XML 檔案儲存在指定的路徑。</span><span class="sxs-lookup"><span data-stu-id="5b0cb-115">The command stores the XML file at the specified path.</span></span>

## <span data-ttu-id="5b0cb-116">參數</span><span class="sxs-lookup"><span data-stu-id="5b0cb-116">PARAMETERS</span></span>

### <span data-ttu-id="5b0cb-117">-識別碼</span><span class="sxs-lookup"><span data-stu-id="5b0cb-117">-Id</span></span>
<span data-ttu-id="5b0cb-118">指定要取得的復原方案 ID。</span><span class="sxs-lookup"><span data-stu-id="5b0cb-118">Specifies the ID of the recovery plan to get.</span></span>

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

### <span data-ttu-id="5b0cb-119">-Path</span><span class="sxs-lookup"><span data-stu-id="5b0cb-119">-Path</span></span>
<span data-ttu-id="5b0cb-120">指定儲存恢復計畫 XML 檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="5b0cb-120">Specifies the full path to store the recovery plan XML file.</span></span>

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

### <span data-ttu-id="5b0cb-121">-設定檔</span><span class="sxs-lookup"><span data-stu-id="5b0cb-121">-Profile</span></span>
<span data-ttu-id="5b0cb-122">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="5b0cb-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5b0cb-123">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="5b0cb-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5b0cb-124">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5b0cb-124">-RecoveryPlan</span></span>
<span data-ttu-id="5b0cb-125">指定要取得其恢復計畫的 **ASRRecoveryPlan** 物件。</span><span class="sxs-lookup"><span data-stu-id="5b0cb-125">Specifies an **ASRRecoveryPlan** object from which to get the recovery plan.</span></span>
<span data-ttu-id="5b0cb-126">若要取得 **ASRRecoveryPlan** 物件，請使用 **AzureSiteRecoveryRecoveryPlan** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5b0cb-126">To obtain an **ASRRecoveryPlan** object, use the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b0cb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b0cb-127">CommonParameters</span></span>
<span data-ttu-id="5b0cb-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5b0cb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b0cb-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5b0cb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b0cb-130">輸入</span><span class="sxs-lookup"><span data-stu-id="5b0cb-130">INPUTS</span></span>

## <span data-ttu-id="5b0cb-131">輸出</span><span class="sxs-lookup"><span data-stu-id="5b0cb-131">OUTPUTS</span></span>

## <span data-ttu-id="5b0cb-132">筆記</span><span class="sxs-lookup"><span data-stu-id="5b0cb-132">NOTES</span></span>

## <span data-ttu-id="5b0cb-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b0cb-133">RELATED LINKS</span></span>

[<span data-ttu-id="5b0cb-134">AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5b0cb-134">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)


