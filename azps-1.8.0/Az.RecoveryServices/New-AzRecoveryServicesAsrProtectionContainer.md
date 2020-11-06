---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 12c5132037e451681434620b65afd6e93235d65b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621106"
---
# <span data-ttu-id="520da-101">New-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="520da-101">New-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="520da-102">摘要</span><span class="sxs-lookup"><span data-stu-id="520da-102">SYNOPSIS</span></span>
<span data-ttu-id="520da-103">在指定的結構中建立 Azure Site Recovery 保護容器。</span><span class="sxs-lookup"><span data-stu-id="520da-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

## <span data-ttu-id="520da-104">句法</span><span class="sxs-lookup"><span data-stu-id="520da-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="520da-105">說明</span><span class="sxs-lookup"><span data-stu-id="520da-105">DESCRIPTION</span></span>
<span data-ttu-id="520da-106">New-AzRecoveryServicesAsrProtectionContainer Cmdlet 會在指定的 Azure Site Recovery 結構下建立保護容器。</span><span class="sxs-lookup"><span data-stu-id="520da-106">The New-AzRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="520da-107">示例</span><span class="sxs-lookup"><span data-stu-id="520da-107">EXAMPLES</span></span>

### <span data-ttu-id="520da-108">範例1</span><span class="sxs-lookup"><span data-stu-id="520da-108">Example 1</span></span>
```
PS C:\> $job = New-AzRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="520da-109">使用指定的參數開始建立保護容器，並傳回用來追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="520da-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="520da-110">參數</span><span class="sxs-lookup"><span data-stu-id="520da-110">PARAMETERS</span></span>

### <span data-ttu-id="520da-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="520da-111">-DefaultProfile</span></span>
<span data-ttu-id="520da-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="520da-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="520da-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="520da-113">-InputObject</span></span>
<span data-ttu-id="520da-114">在指定的輸入物件 (Azure Fabric) 中建立禁止複製容器。</span><span class="sxs-lookup"><span data-stu-id="520da-114">Creates the replication protection container in specifed input Object (Azure Fabric).</span></span>

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

### <span data-ttu-id="520da-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="520da-115">-Name</span></span>
<span data-ttu-id="520da-116">保護容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="520da-116">Name of the protection container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="520da-117">-確認</span><span class="sxs-lookup"><span data-stu-id="520da-117">-Confirm</span></span>
<span data-ttu-id="520da-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="520da-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="520da-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="520da-119">-WhatIf</span></span>
<span data-ttu-id="520da-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="520da-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="520da-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="520da-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="520da-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="520da-122">CommonParameters</span></span>
<span data-ttu-id="520da-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="520da-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="520da-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="520da-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="520da-125">輸入</span><span class="sxs-lookup"><span data-stu-id="520da-125">INPUTS</span></span>

### <span data-ttu-id="520da-126">RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="520da-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="520da-127">輸出</span><span class="sxs-lookup"><span data-stu-id="520da-127">OUTPUTS</span></span>

### <span data-ttu-id="520da-128">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="520da-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="520da-129">筆記</span><span class="sxs-lookup"><span data-stu-id="520da-129">NOTES</span></span>

## <span data-ttu-id="520da-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="520da-130">RELATED LINKS</span></span>
