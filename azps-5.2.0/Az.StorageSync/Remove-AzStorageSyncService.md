---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: f64c085f742eeabea235660d4af7ba6bd5970fdf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283312"
---
# <span data-ttu-id="f7209-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="f7209-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="f7209-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f7209-102">SYNOPSIS</span></span>
<span data-ttu-id="f7209-103">這個命令會刪除指定的儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="f7209-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="f7209-104">句法</span><span class="sxs-lookup"><span data-stu-id="f7209-104">SYNTAX</span></span>

### <span data-ttu-id="f7209-105">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f7209-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7209-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7209-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7209-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7209-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7209-108">說明</span><span class="sxs-lookup"><span data-stu-id="f7209-108">DESCRIPTION</span></span>
<span data-ttu-id="f7209-109">這個命令會刪除指定的儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="f7209-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="f7209-110">只有在先刪除所有包含的同步處理群組與已註冊的伺服器時，才能移除儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="f7209-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="f7209-111">示例</span><span class="sxs-lookup"><span data-stu-id="f7209-111">EXAMPLES</span></span>

### <span data-ttu-id="f7209-112">範例1</span><span class="sxs-lookup"><span data-stu-id="f7209-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="f7209-113">這個命令會移除儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="f7209-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="f7209-114">參數</span><span class="sxs-lookup"><span data-stu-id="f7209-114">PARAMETERS</span></span>

### <span data-ttu-id="f7209-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7209-115">-AsJob</span></span>
<span data-ttu-id="f7209-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f7209-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7209-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7209-117">-DefaultProfile</span></span>
<span data-ttu-id="f7209-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7209-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7209-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f7209-119">-Force</span></span>
<span data-ttu-id="f7209-120">[提供-強制略過此命令的確認]。</span><span class="sxs-lookup"><span data-stu-id="f7209-120">Supply -Force to skip confirmation of this command.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7209-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7209-121">-InputObject</span></span>
<span data-ttu-id="f7209-122">StorageSyncService 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="f7209-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7209-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="f7209-123">-Name</span></span>
<span data-ttu-id="f7209-124">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7209-124">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: StorageSyncServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7209-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7209-125">-PassThru</span></span>
<span data-ttu-id="f7209-126">在正常執行中，此 Cmdlet 在成功時不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f7209-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="f7209-127">如果您提供 PassThru 參數，則在成功執行之後，Cmdlet 會將值寫入管道。</span><span class="sxs-lookup"><span data-stu-id="f7209-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="f7209-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7209-128">-ResourceGroupName</span></span>
<span data-ttu-id="f7209-129">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f7209-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7209-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7209-130">-ResourceId</span></span>
<span data-ttu-id="f7209-131">StorageSyncService 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f7209-131">StorageSyncService Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7209-132">-確認</span><span class="sxs-lookup"><span data-stu-id="f7209-132">-Confirm</span></span>
<span data-ttu-id="f7209-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f7209-133">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7209-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7209-134">-WhatIf</span></span>
<span data-ttu-id="f7209-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f7209-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7209-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f7209-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7209-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7209-137">CommonParameters</span></span>
<span data-ttu-id="f7209-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f7209-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7209-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f7209-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7209-140">輸入</span><span class="sxs-lookup"><span data-stu-id="f7209-140">INPUTS</span></span>

### <span data-ttu-id="f7209-141">PSStorageSyncService 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="f7209-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="f7209-142">System.object</span><span class="sxs-lookup"><span data-stu-id="f7209-142">System.String</span></span>

### <span data-ttu-id="f7209-143">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="f7209-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f7209-144">輸出</span><span class="sxs-lookup"><span data-stu-id="f7209-144">OUTPUTS</span></span>

### <span data-ttu-id="f7209-145">System.object</span><span class="sxs-lookup"><span data-stu-id="f7209-145">System.Object</span></span>
## <span data-ttu-id="f7209-146">筆記</span><span class="sxs-lookup"><span data-stu-id="f7209-146">NOTES</span></span>

## <span data-ttu-id="f7209-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7209-147">RELATED LINKS</span></span>
