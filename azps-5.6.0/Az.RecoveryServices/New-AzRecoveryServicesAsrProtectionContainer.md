---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 22ade5e749909683ff2de93065ccf458ab2ec73f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903101"
---
# <span data-ttu-id="f7364-101">New-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f7364-101">New-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="f7364-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f7364-102">SYNOPSIS</span></span>
<span data-ttu-id="f7364-103">在指定的結構內建立 Azure 網站復原保護容器。</span><span class="sxs-lookup"><span data-stu-id="f7364-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

## <span data-ttu-id="f7364-104">語法</span><span class="sxs-lookup"><span data-stu-id="f7364-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7364-105">描述</span><span class="sxs-lookup"><span data-stu-id="f7364-105">DESCRIPTION</span></span>
<span data-ttu-id="f7364-106">此New-AzRecoveryServicesAsrProtectionContainer Cmdlet 會建立指定 Azure 網站修復結構下的保護容器。</span><span class="sxs-lookup"><span data-stu-id="f7364-106">The New-AzRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="f7364-107">例子</span><span class="sxs-lookup"><span data-stu-id="f7364-107">EXAMPLES</span></span>

### <span data-ttu-id="f7364-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="f7364-108">Example 1</span></span>
```
PS C:\> $job = New-AzRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="f7364-109">使用指定的參數開始建立保護容器，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="f7364-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f7364-110">參數</span><span class="sxs-lookup"><span data-stu-id="f7364-110">PARAMETERS</span></span>

### <span data-ttu-id="f7364-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7364-111">-DefaultProfile</span></span>
<span data-ttu-id="f7364-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7364-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7364-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7364-113">-InputObject</span></span>
<span data-ttu-id="f7364-114">在指定的輸入物件中建立禁止複製容器 (Azure Fabric) 。</span><span class="sxs-lookup"><span data-stu-id="f7364-114">Creates the replication protection container in specified input Object (Azure Fabric).</span></span>

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

### <span data-ttu-id="f7364-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="f7364-115">-Name</span></span>
<span data-ttu-id="f7364-116">保護容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7364-116">Name of the protection container.</span></span>

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

### <span data-ttu-id="f7364-117">-確認</span><span class="sxs-lookup"><span data-stu-id="f7364-117">-Confirm</span></span>
<span data-ttu-id="f7364-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f7364-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7364-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7364-119">-WhatIf</span></span>
<span data-ttu-id="f7364-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f7364-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7364-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f7364-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7364-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7364-122">CommonParameters</span></span>
<span data-ttu-id="f7364-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f7364-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7364-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7364-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7364-125">輸入</span><span class="sxs-lookup"><span data-stu-id="f7364-125">INPUTS</span></span>

### <span data-ttu-id="f7364-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="f7364-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="f7364-127">輸出</span><span class="sxs-lookup"><span data-stu-id="f7364-127">OUTPUTS</span></span>

### <span data-ttu-id="f7364-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="f7364-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f7364-129">筆記</span><span class="sxs-lookup"><span data-stu-id="f7364-129">NOTES</span></span>

## <span data-ttu-id="f7364-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7364-130">RELATED LINKS</span></span>
