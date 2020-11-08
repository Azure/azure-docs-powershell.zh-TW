---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: 630dc1a3a14beec147dec3f7bd2601ed0666ad78
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970832"
---
# <span data-ttu-id="48681-101">Copy-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="48681-101">Copy-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="48681-102">摘要</span><span class="sxs-lookup"><span data-stu-id="48681-102">SYNOPSIS</span></span>
<span data-ttu-id="48681-103">將一個區域中的電子倉庫的資料複製到另一個區域的電子倉庫中。</span><span class="sxs-lookup"><span data-stu-id="48681-103">Copies data from a vault in one region to a vault in another region.</span></span>

## <span data-ttu-id="48681-104">句法</span><span class="sxs-lookup"><span data-stu-id="48681-104">SYNTAX</span></span>

```
Copy-AzRecoveryServicesVault [-Force] [-DefaultProfile <IAzureContextContainer>] [-SourceVault] <ARSVault>
 [-TargetVault] <ARSVault> [-RetryOnlyFailed] [<CommonParameters>]
```

## <span data-ttu-id="48681-105">說明</span><span class="sxs-lookup"><span data-stu-id="48681-105">DESCRIPTION</span></span>
<span data-ttu-id="48681-106">**AzRecoveryServicesVault** Cmdlet 會將一個區域中的電子倉庫的資料複製到另一個區域的電子倉庫中。</span><span class="sxs-lookup"><span data-stu-id="48681-106">The **Copy-AzRecoveryServicesVault** cmdlet copies data from a vault in one region to a vault in another region.</span></span> <span data-ttu-id="48681-107">目前我們只支援保存庫層級資料移動。</span><span class="sxs-lookup"><span data-stu-id="48681-107">Currently we only support vault level data move.</span></span>

## <span data-ttu-id="48681-108">示例</span><span class="sxs-lookup"><span data-stu-id="48681-108">EXAMPLES</span></span>

### <span data-ttu-id="48681-109">範例1：將資料從 vault1 複製到 vault2</span><span class="sxs-lookup"><span data-stu-id="48681-109">Example 1: Copy data from vault1 to vault2</span></span>
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```git 

The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.
The second command triggers a complete data move from vault1 to vault2. 

### Example 2: Copy data from vault1 to vault2 with only failed items
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
```git 

The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.
The second command triggers a partial data move from vault1 to vault2 with only those items which failed in previous move operations.

## PARAMETERS

### -DefaultProfile
The credentials, account, tenant, and subscription used for communication with Azure.

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

### <span data-ttu-id="48681-110">-Force</span><span class="sxs-lookup"><span data-stu-id="48681-110">-Force</span></span>
<span data-ttu-id="48681-111">強制執行資料移動操作 (防止確認對話方塊) ，而不要求確認目標保存庫儲存冗余類型。</span><span class="sxs-lookup"><span data-stu-id="48681-111">Forces the data move operation (prevents confirmation dialog) without asking confirmation for target vault storage redundancy type.</span></span> <span data-ttu-id="48681-112">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="48681-112">This parameter is optional.</span></span> 

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

### <span data-ttu-id="48681-113">-RetryOnlyFailed</span><span class="sxs-lookup"><span data-stu-id="48681-113">-RetryOnlyFailed</span></span>
<span data-ttu-id="48681-114">[切換參數] 只會針對來源電子倉庫中尚未移動的容器移動資料。</span><span class="sxs-lookup"><span data-stu-id="48681-114">Switch parameter to try data move only for containers in the source vault which are not yet moved.</span></span>

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

### <span data-ttu-id="48681-115">-SourceVault</span><span class="sxs-lookup"><span data-stu-id="48681-115">-SourceVault</span></span>
<span data-ttu-id="48681-116">要移動的來源電子倉庫物件。</span><span class="sxs-lookup"><span data-stu-id="48681-116">The source vault object to be moved.</span></span>

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

### <span data-ttu-id="48681-117">-TargetVault</span><span class="sxs-lookup"><span data-stu-id="48681-117">-TargetVault</span></span>
<span data-ttu-id="48681-118">必須移動資料的目標電子倉庫物件。</span><span class="sxs-lookup"><span data-stu-id="48681-118">The target vault object where the data has to be moved.</span></span>

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

### <span data-ttu-id="48681-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48681-119">CommonParameters</span></span>
<span data-ttu-id="48681-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="48681-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48681-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="48681-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48681-122">輸入</span><span class="sxs-lookup"><span data-stu-id="48681-122">INPUTS</span></span>

### <span data-ttu-id="48681-123">ARSVault 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48681-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="48681-124">輸出</span><span class="sxs-lookup"><span data-stu-id="48681-124">OUTPUTS</span></span>

### <span data-ttu-id="48681-125">System.object</span><span class="sxs-lookup"><span data-stu-id="48681-125">System.String</span></span>

## <span data-ttu-id="48681-126">筆記</span><span class="sxs-lookup"><span data-stu-id="48681-126">NOTES</span></span>

## <span data-ttu-id="48681-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="48681-127">RELATED LINKS</span></span>
