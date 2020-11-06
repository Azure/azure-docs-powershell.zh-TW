---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 8a7b36b67b0ec1721da36dfeba920b556892c5f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454572"
---
# <span data-ttu-id="ebcbe-101">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="ebcbe-101">Remove-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="ebcbe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ebcbe-102">SYNOPSIS</span></span>
<span data-ttu-id="ebcbe-103">從 [恢復服務] 保存庫刪除指定的 Azure 網站復原結構。</span><span class="sxs-lookup"><span data-stu-id="ebcbe-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebcbe-104">句法</span><span class="sxs-lookup"><span data-stu-id="ebcbe-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebcbe-105">說明</span><span class="sxs-lookup"><span data-stu-id="ebcbe-105">DESCRIPTION</span></span>
<span data-ttu-id="ebcbe-106">**AzureRmRecoveryServicesAsrFabric** Cmdlet 會從 [恢復服務] 保存庫中移除指定的 Azure 網站復原結構。</span><span class="sxs-lookup"><span data-stu-id="ebcbe-106">The **Remove-AzureRmRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="ebcbe-107">示例</span><span class="sxs-lookup"><span data-stu-id="ebcbe-107">EXAMPLES</span></span>

### <span data-ttu-id="ebcbe-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ebcbe-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="ebcbe-109">開始刪除指定的結構，並傳回用於追蹤操作的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="ebcbe-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="ebcbe-110">參數</span><span class="sxs-lookup"><span data-stu-id="ebcbe-110">PARAMETERS</span></span>

### <span data-ttu-id="ebcbe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebcbe-111">-DefaultProfile</span></span>
<span data-ttu-id="ebcbe-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ebcbe-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebcbe-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ebcbe-113">-Force</span></span>
<span data-ttu-id="ebcbe-114">強制執行命令，但不提供額外的警告。</span><span class="sxs-lookup"><span data-stu-id="ebcbe-114">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebcbe-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebcbe-115">-InputObject</span></span>
<span data-ttu-id="ebcbe-116">Cmdlet 的輸入物件：對應到要刪除之結構的 ASR fabric 物件。</span><span class="sxs-lookup"><span data-stu-id="ebcbe-116">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebcbe-117">-確認</span><span class="sxs-lookup"><span data-stu-id="ebcbe-117">-Confirm</span></span>
<span data-ttu-id="ebcbe-118">指定是否需要確認。</span><span class="sxs-lookup"><span data-stu-id="ebcbe-118">Specify if confirmation is required.</span></span> <span data-ttu-id="ebcbe-119">將確認參數的值設定為 [$false]，以略過確認。</span><span class="sxs-lookup"><span data-stu-id="ebcbe-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebcbe-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebcbe-120">-WhatIf</span></span>
<span data-ttu-id="ebcbe-121">顯示在未實際執行 Cmdlet 的情況下執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ebcbe-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebcbe-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebcbe-122">CommonParameters</span></span>
<span data-ttu-id="ebcbe-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ebcbe-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebcbe-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ebcbe-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebcbe-125">輸入</span><span class="sxs-lookup"><span data-stu-id="ebcbe-125">INPUTS</span></span>

### <span data-ttu-id="ebcbe-126">RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="ebcbe-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="ebcbe-127">輸出</span><span class="sxs-lookup"><span data-stu-id="ebcbe-127">OUTPUTS</span></span>

### <span data-ttu-id="ebcbe-128">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ebcbe-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ebcbe-129">筆記</span><span class="sxs-lookup"><span data-stu-id="ebcbe-129">NOTES</span></span>

## <span data-ttu-id="ebcbe-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="ebcbe-130">RELATED LINKS</span></span>

[<span data-ttu-id="ebcbe-131">AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="ebcbe-131">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="ebcbe-132">新-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="ebcbe-132">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)
