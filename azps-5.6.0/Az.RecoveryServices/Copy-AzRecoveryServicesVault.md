---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: 5b4c7153a844bdc10d2ec487e51ef9f07be0c5c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903986"
---
# <span data-ttu-id="12e60-101">Copy-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="12e60-101">Copy-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="12e60-102">簡介</span><span class="sxs-lookup"><span data-stu-id="12e60-102">SYNOPSIS</span></span>
<span data-ttu-id="12e60-103">將資料從一個地區的保存庫複製到另一個地區的保存庫。</span><span class="sxs-lookup"><span data-stu-id="12e60-103">Copies data from a vault in one region to a vault in another region.</span></span>

## <span data-ttu-id="12e60-104">語法</span><span class="sxs-lookup"><span data-stu-id="12e60-104">SYNTAX</span></span>

```
Copy-AzRecoveryServicesVault [-Force] [-DefaultProfile <IAzureContextContainer>] [-SourceVault] <ARSVault>
 [-TargetVault] <ARSVault> [-RetryOnlyFailed] [<CommonParameters>]
```

## <span data-ttu-id="12e60-105">描述</span><span class="sxs-lookup"><span data-stu-id="12e60-105">DESCRIPTION</span></span>
<span data-ttu-id="12e60-106">**Copy-AzRecoveryServicesVault** Cmdlet 將資料從一個地區的保存庫複製到另一個地區的保存庫。</span><span class="sxs-lookup"><span data-stu-id="12e60-106">The **Copy-AzRecoveryServicesVault** cmdlet copies data from a vault in one region to a vault in another region.</span></span> <span data-ttu-id="12e60-107">目前我們僅支援函式庫層級資料移動。</span><span class="sxs-lookup"><span data-stu-id="12e60-107">Currently we only support vault level data move.</span></span>

## <span data-ttu-id="12e60-108">例子</span><span class="sxs-lookup"><span data-stu-id="12e60-108">EXAMPLES</span></span>

### <span data-ttu-id="12e60-109">範例 1：將資料從保存庫1 複製到保存庫2</span><span class="sxs-lookup"><span data-stu-id="12e60-109">Example 1: Copy data from vault1 to vault2</span></span>
```
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```

<span data-ttu-id="12e60-110">前兩個 Cmdlet 分別會抓取修復服務儲存庫 - vault1 和 vault2。</span><span class="sxs-lookup"><span data-stu-id="12e60-110">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="12e60-111">第二個命令會觸發從 vault1 到 vault2 的完整資料移動。</span><span class="sxs-lookup"><span data-stu-id="12e60-111">The second command triggers a complete data move from vault1 to vault2.</span></span> 

### <span data-ttu-id="12e60-112">範例 2：將資料從保存庫1 複製到保存庫2，只包含失敗的專案</span><span class="sxs-lookup"><span data-stu-id="12e60-112">Example 2: Copy data from vault1 to vault2 with only failed items</span></span>
```
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
```

<span data-ttu-id="12e60-113">前兩個 Cmdlet 分別會抓取修復服務儲存庫 - vault1 和 vault2。</span><span class="sxs-lookup"><span data-stu-id="12e60-113">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="12e60-114">第二個命令會觸發部分資料從 vault1 移至 vault2，只包含先前移動作業失敗的專案。</span><span class="sxs-lookup"><span data-stu-id="12e60-114">The second command triggers a partial data move from vault1 to vault2 with only those items which failed in previous move operations.</span></span>

## <span data-ttu-id="12e60-115">參數</span><span class="sxs-lookup"><span data-stu-id="12e60-115">PARAMETERS</span></span>

### <span data-ttu-id="12e60-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12e60-116">-DefaultProfile</span></span>
<span data-ttu-id="12e60-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="12e60-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12e60-118">-強制</span><span class="sxs-lookup"><span data-stu-id="12e60-118">-Force</span></span>
<span data-ttu-id="12e60-119">強制資料移動作業 (確認對話方塊，) 確認目標保存庫儲存冗余類型。</span><span class="sxs-lookup"><span data-stu-id="12e60-119">Forces the data move operation (prevents confirmation dialog) without asking confirmation for target vault storage redundancy type.</span></span> <span data-ttu-id="12e60-120">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="12e60-120">This parameter is optional.</span></span> 

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

### <span data-ttu-id="12e60-121">-重試OnlyFailed</span><span class="sxs-lookup"><span data-stu-id="12e60-121">-RetryOnlyFailed</span></span>
<span data-ttu-id="12e60-122">切換參數，只針對尚未移動的來源庫中的容器嘗試資料移動。</span><span class="sxs-lookup"><span data-stu-id="12e60-122">Switch parameter to try data move only for containers in the source vault which are not yet moved.</span></span>

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

### <span data-ttu-id="12e60-123">-SourceVault</span><span class="sxs-lookup"><span data-stu-id="12e60-123">-SourceVault</span></span>
<span data-ttu-id="12e60-124">要移動的來源庫物件。</span><span class="sxs-lookup"><span data-stu-id="12e60-124">The source vault object to be moved.</span></span>

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

### <span data-ttu-id="12e60-125">-TargetVault</span><span class="sxs-lookup"><span data-stu-id="12e60-125">-TargetVault</span></span>
<span data-ttu-id="12e60-126">資料必須移動的目標庫物件。</span><span class="sxs-lookup"><span data-stu-id="12e60-126">The target vault object where the data has to be moved.</span></span>

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

### <span data-ttu-id="12e60-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e60-127">CommonParameters</span></span>
<span data-ttu-id="12e60-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="12e60-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e60-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12e60-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e60-130">輸入</span><span class="sxs-lookup"><span data-stu-id="12e60-130">INPUTS</span></span>

### <span data-ttu-id="12e60-131">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="12e60-131">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="12e60-132">輸出</span><span class="sxs-lookup"><span data-stu-id="12e60-132">OUTPUTS</span></span>

### <span data-ttu-id="12e60-133">System.String</span><span class="sxs-lookup"><span data-stu-id="12e60-133">System.String</span></span>

## <span data-ttu-id="12e60-134">筆記</span><span class="sxs-lookup"><span data-stu-id="12e60-134">NOTES</span></span>

## <span data-ttu-id="12e60-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="12e60-135">RELATED LINKS</span></span>
