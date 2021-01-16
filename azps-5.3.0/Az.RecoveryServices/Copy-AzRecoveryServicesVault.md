---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: 68c2914c694dbfb89044597fc35582a83f426b6c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435654"
---
# <span data-ttu-id="01fd2-101">Copy-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="01fd2-101">Copy-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="01fd2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="01fd2-102">SYNOPSIS</span></span>
<span data-ttu-id="01fd2-103">將一個區域中的電子倉庫的資料複製到另一個區域的電子倉庫中。</span><span class="sxs-lookup"><span data-stu-id="01fd2-103">Copies data from a vault in one region to a vault in another region.</span></span>

## <span data-ttu-id="01fd2-104">句法</span><span class="sxs-lookup"><span data-stu-id="01fd2-104">SYNTAX</span></span>

```
Copy-AzRecoveryServicesVault [-Force] [-DefaultProfile <IAzureContextContainer>] [-SourceVault] <ARSVault>
 [-TargetVault] <ARSVault> [-RetryOnlyFailed] [<CommonParameters>]
```

## <span data-ttu-id="01fd2-105">說明</span><span class="sxs-lookup"><span data-stu-id="01fd2-105">DESCRIPTION</span></span>
<span data-ttu-id="01fd2-106">**AzRecoveryServicesVault** Cmdlet 會將一個區域中的電子倉庫的資料複製到另一個區域的電子倉庫中。</span><span class="sxs-lookup"><span data-stu-id="01fd2-106">The **Copy-AzRecoveryServicesVault** cmdlet copies data from a vault in one region to a vault in another region.</span></span> <span data-ttu-id="01fd2-107">目前我們只支援保存庫層級資料移動。</span><span class="sxs-lookup"><span data-stu-id="01fd2-107">Currently we only support vault level data move.</span></span>

## <span data-ttu-id="01fd2-108">示例</span><span class="sxs-lookup"><span data-stu-id="01fd2-108">EXAMPLES</span></span>

### <span data-ttu-id="01fd2-109">範例1：將資料從 vault1 複製到 vault2</span><span class="sxs-lookup"><span data-stu-id="01fd2-109">Example 1: Copy data from vault1 to vault2</span></span>
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```

<span data-ttu-id="01fd2-110">前兩個 Cmdlet 分別提取復原服務電子倉庫-vault1 和 vault2。</span><span class="sxs-lookup"><span data-stu-id="01fd2-110">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="01fd2-111">第二個命令會觸發完整的資料從 vault1 移至 vault2。</span><span class="sxs-lookup"><span data-stu-id="01fd2-111">The second command triggers a complete data move from vault1 to vault2.</span></span> 

### <span data-ttu-id="01fd2-112">範例2：將資料從 vault1 複製到 vault2，只有失敗的專案</span><span class="sxs-lookup"><span data-stu-id="01fd2-112">Example 2: Copy data from vault1 to vault2 with only failed items</span></span>
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
``` 

<span data-ttu-id="01fd2-113">前兩個 Cmdlet 分別提取復原服務電子倉庫-vault1 和 vault2。</span><span class="sxs-lookup"><span data-stu-id="01fd2-113">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="01fd2-114">第二個命令會觸發部分資料從 vault1 移至 vault2，只有那些在先前的移動作業中失敗的專案。</span><span class="sxs-lookup"><span data-stu-id="01fd2-114">The second command triggers a partial data move from vault1 to vault2 with only those items which failed in previous move operations.</span></span>

## <span data-ttu-id="01fd2-115">參數</span><span class="sxs-lookup"><span data-stu-id="01fd2-115">PARAMETERS</span></span>

### <span data-ttu-id="01fd2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01fd2-116">-DefaultProfile</span></span>
<span data-ttu-id="01fd2-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="01fd2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01fd2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="01fd2-118">-Force</span></span>
<span data-ttu-id="01fd2-119">強制執行資料移動操作 (防止確認對話方塊) ，而不要求確認目標保存庫儲存冗余類型。</span><span class="sxs-lookup"><span data-stu-id="01fd2-119">Forces the data move operation (prevents confirmation dialog) without asking confirmation for target vault storage redundancy type.</span></span> <span data-ttu-id="01fd2-120">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="01fd2-120">This parameter is optional.</span></span> 

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

### <span data-ttu-id="01fd2-121">-RetryOnlyFailed</span><span class="sxs-lookup"><span data-stu-id="01fd2-121">-RetryOnlyFailed</span></span>
<span data-ttu-id="01fd2-122">[切換參數] 只會針對來源電子倉庫中尚未移動的容器移動資料。</span><span class="sxs-lookup"><span data-stu-id="01fd2-122">Switch parameter to try data move only for containers in the source vault which are not yet moved.</span></span>

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

### <span data-ttu-id="01fd2-123">-SourceVault</span><span class="sxs-lookup"><span data-stu-id="01fd2-123">-SourceVault</span></span>
<span data-ttu-id="01fd2-124">要移動的來源電子倉庫物件。</span><span class="sxs-lookup"><span data-stu-id="01fd2-124">The source vault object to be moved.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01fd2-125">-TargetVault</span><span class="sxs-lookup"><span data-stu-id="01fd2-125">-TargetVault</span></span>
<span data-ttu-id="01fd2-126">必須移動資料的目標電子倉庫物件。</span><span class="sxs-lookup"><span data-stu-id="01fd2-126">The target vault object where the data has to be moved.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01fd2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01fd2-127">CommonParameters</span></span>
<span data-ttu-id="01fd2-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="01fd2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01fd2-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="01fd2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01fd2-130">輸入</span><span class="sxs-lookup"><span data-stu-id="01fd2-130">INPUTS</span></span>

### <span data-ttu-id="01fd2-131">ARSVault 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="01fd2-131">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="01fd2-132">輸出</span><span class="sxs-lookup"><span data-stu-id="01fd2-132">OUTPUTS</span></span>

### <span data-ttu-id="01fd2-133">System.object</span><span class="sxs-lookup"><span data-stu-id="01fd2-133">System.String</span></span>

## <span data-ttu-id="01fd2-134">筆記</span><span class="sxs-lookup"><span data-stu-id="01fd2-134">NOTES</span></span>

## <span data-ttu-id="01fd2-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="01fd2-135">RELATED LINKS</span></span>
