---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 45979620ea4067af3fc906dfd7348d27b4850f06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450543"
---
# <span data-ttu-id="4d414-101">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="4d414-101">Remove-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="4d414-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4d414-102">SYNOPSIS</span></span>
<span data-ttu-id="4d414-103">從 [恢復服務] 保存庫刪除指定的 Azure 網站復原結構。</span><span class="sxs-lookup"><span data-stu-id="4d414-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d414-104">句法</span><span class="sxs-lookup"><span data-stu-id="4d414-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d414-105">說明</span><span class="sxs-lookup"><span data-stu-id="4d414-105">DESCRIPTION</span></span>
<span data-ttu-id="4d414-106">**AzureRmRecoveryServicesAsrFabric** Cmdlet 會從 [恢復服務] 保存庫中移除指定的 Azure 網站復原結構。</span><span class="sxs-lookup"><span data-stu-id="4d414-106">The **Remove-AzureRmRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="4d414-107">示例</span><span class="sxs-lookup"><span data-stu-id="4d414-107">EXAMPLES</span></span>

### <span data-ttu-id="4d414-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4d414-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="4d414-109">開始刪除指定的結構，並傳回用於追蹤操作的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="4d414-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="4d414-110">參數</span><span class="sxs-lookup"><span data-stu-id="4d414-110">PARAMETERS</span></span>

### <span data-ttu-id="4d414-111">-確認</span><span class="sxs-lookup"><span data-stu-id="4d414-111">-Confirm</span></span>
<span data-ttu-id="4d414-112">指定是否需要確認。</span><span class="sxs-lookup"><span data-stu-id="4d414-112">Specify if confirmation is required.</span></span> <span data-ttu-id="4d414-113">將確認參數的值設定為 [$false]，以略過確認。</span><span class="sxs-lookup"><span data-stu-id="4d414-113">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d414-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d414-114">-DefaultProfile</span></span>
<span data-ttu-id="4d414-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4d414-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d414-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4d414-116">-Force</span></span>
<span data-ttu-id="4d414-117">強制執行命令，但不提供額外的警告。</span><span class="sxs-lookup"><span data-stu-id="4d414-117">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="4d414-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d414-118">-InputObject</span></span>
<span data-ttu-id="4d414-119">Cmdlet 的輸入物件：對應到要刪除之結構的 ASR fabric 物件。</span><span class="sxs-lookup"><span data-stu-id="4d414-119">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d414-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d414-120">-WhatIf</span></span>
<span data-ttu-id="4d414-121">顯示在未實際執行 Cmdlet 的情況下執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4d414-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d414-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d414-122">CommonParameters</span></span>
<span data-ttu-id="4d414-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4d414-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d414-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4d414-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d414-125">輸入</span><span class="sxs-lookup"><span data-stu-id="4d414-125">INPUTS</span></span>

### <span data-ttu-id="4d414-126">RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="4d414-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="4d414-127">輸出</span><span class="sxs-lookup"><span data-stu-id="4d414-127">OUTPUTS</span></span>

### <span data-ttu-id="4d414-128">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4d414-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4d414-129">筆記</span><span class="sxs-lookup"><span data-stu-id="4d414-129">NOTES</span></span>

## <span data-ttu-id="4d414-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="4d414-130">RELATED LINKS</span></span>

[<span data-ttu-id="4d414-131">AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="4d414-131">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="4d414-132">新-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="4d414-132">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)
