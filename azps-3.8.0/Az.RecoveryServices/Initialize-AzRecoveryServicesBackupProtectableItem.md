---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/initialize-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 8bc2286cf6df736ee54390447e83f0337c031001
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966154"
---
# <span data-ttu-id="c33b7-101">Initialize-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="c33b7-101">Initialize-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="c33b7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c33b7-102">SYNOPSIS</span></span>
<span data-ttu-id="c33b7-103">這個命令會在指定的容器中觸發發現指定工作負荷類型的任何未受保護專案。</span><span class="sxs-lookup"><span data-stu-id="c33b7-103">This command triggers the discovery of any unprotected items of the given workload type in the given container.</span></span> <span data-ttu-id="c33b7-104">如果資料庫應用程式不是自動受保護的，請使用此命令，在新資料庫新增後進行探索並繼續保護它們。</span><span class="sxs-lookup"><span data-stu-id="c33b7-104">If the DB application is not auto-protected use this command to discover new DBs whenever they are added and proceed to protect them.</span></span>

## <span data-ttu-id="c33b7-105">句法</span><span class="sxs-lookup"><span data-stu-id="c33b7-105">SYNTAX</span></span>

```
Initialize-AzRecoveryServicesBackupProtectableItem [-Container] <ContainerBase> [-WorkloadType] <WorkloadType>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c33b7-106">說明</span><span class="sxs-lookup"><span data-stu-id="c33b7-106">DESCRIPTION</span></span>
<span data-ttu-id="c33b7-107">容器中特定工作負載的 Cmdlet enquires。</span><span class="sxs-lookup"><span data-stu-id="c33b7-107">the cmdlet enquires for specific workloads within a container.</span></span> <span data-ttu-id="c33b7-108">這會觸發建立可保護專案的作業。</span><span class="sxs-lookup"><span data-stu-id="c33b7-108">This triggers an operation which creates protectable items.</span></span>

## <span data-ttu-id="c33b7-109">示例</span><span class="sxs-lookup"><span data-stu-id="c33b7-109">EXAMPLES</span></span>

### <span data-ttu-id="c33b7-110">範例1</span><span class="sxs-lookup"><span data-stu-id="c33b7-110">Example 1</span></span>
```
PS C:\> Initialize-AzRecoveryServicesProtectableItem -Container $Container -WorkloadType "MSSQL"
```

<span data-ttu-id="c33b7-111">這個 Cmdlet 會針對新的可保護專案執行探索作業。</span><span class="sxs-lookup"><span data-stu-id="c33b7-111">The cmdlet executes a discovery operation for new protectable items.</span></span>

## <span data-ttu-id="c33b7-112">參數</span><span class="sxs-lookup"><span data-stu-id="c33b7-112">PARAMETERS</span></span>

### <span data-ttu-id="c33b7-113">-容器</span><span class="sxs-lookup"><span data-stu-id="c33b7-113">-Container</span></span>
<span data-ttu-id="c33b7-114">專案所在的容器</span><span class="sxs-lookup"><span data-stu-id="c33b7-114">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c33b7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c33b7-115">-DefaultProfile</span></span>
<span data-ttu-id="c33b7-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c33b7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c33b7-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c33b7-117">-PassThru</span></span>
<span data-ttu-id="c33b7-118">返回要刪除的容器。</span><span class="sxs-lookup"><span data-stu-id="c33b7-118">Return the container to be deleted.</span></span>

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

### <span data-ttu-id="c33b7-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="c33b7-119">-VaultId</span></span>
<span data-ttu-id="c33b7-120">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="c33b7-120">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c33b7-121">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="c33b7-121">-WorkloadType</span></span>
<span data-ttu-id="c33b7-122">資源的工作量類型 (例如： Add-azurevm、WindowsServer、AzureFiles、MSSQL) 。</span><span class="sxs-lookup"><span data-stu-id="c33b7-122">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c33b7-123">-確認</span><span class="sxs-lookup"><span data-stu-id="c33b7-123">-Confirm</span></span>
<span data-ttu-id="c33b7-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c33b7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c33b7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c33b7-125">-WhatIf</span></span>
<span data-ttu-id="c33b7-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c33b7-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c33b7-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c33b7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c33b7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c33b7-128">CommonParameters</span></span>
<span data-ttu-id="c33b7-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c33b7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c33b7-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c33b7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c33b7-131">輸入</span><span class="sxs-lookup"><span data-stu-id="c33b7-131">INPUTS</span></span>

### <span data-ttu-id="c33b7-132">ContainerBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="c33b7-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="c33b7-133">System.object</span><span class="sxs-lookup"><span data-stu-id="c33b7-133">System.String</span></span>

## <span data-ttu-id="c33b7-134">輸出</span><span class="sxs-lookup"><span data-stu-id="c33b7-134">OUTPUTS</span></span>

### <span data-ttu-id="c33b7-135">ItemBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="c33b7-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="c33b7-136">筆記</span><span class="sxs-lookup"><span data-stu-id="c33b7-136">NOTES</span></span>

## <span data-ttu-id="c33b7-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="c33b7-137">RELATED LINKS</span></span>
