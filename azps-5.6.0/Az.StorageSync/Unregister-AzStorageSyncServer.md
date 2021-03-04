---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: 5ebcdee62997ed678b9696264a40076a40c36342
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907417"
---
# <span data-ttu-id="e305d-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="e305d-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="e305d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e305d-102">SYNOPSIS</span></span>
<span data-ttu-id="e305d-103">警告：取消註冊伺服器會導致此伺服器上所有伺服器端點的串聯刪除。</span><span class="sxs-lookup"><span data-stu-id="e305d-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="e305d-104">此命令會從儲存同步處理服務取消註冊伺服器。</span><span class="sxs-lookup"><span data-stu-id="e305d-104">This command will unregister a server from it's storage sync service.</span></span>

## <span data-ttu-id="e305d-105">語法</span><span class="sxs-lookup"><span data-stu-id="e305d-105">SYNTAX</span></span>

### <span data-ttu-id="e305d-106">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e305d-106">StringParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e305d-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e305d-107">InputObjectParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e305d-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e305d-108">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e305d-109">描述</span><span class="sxs-lookup"><span data-stu-id="e305d-109">DESCRIPTION</span></span>
<span data-ttu-id="e305d-110">此命令會從儲存同步處理服務取消註冊伺服器。</span><span class="sxs-lookup"><span data-stu-id="e305d-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="e305d-111">警告：取消註冊伺服器會導致此伺服器上所有伺服器端點的串聯刪除。</span><span class="sxs-lookup"><span data-stu-id="e305d-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="e305d-112">只有在您確定此伺服器上不再同步處理任何路徑時，才應該會叫這個路徑。</span><span class="sxs-lookup"><span data-stu-id="e305d-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="e305d-113">例子</span><span class="sxs-lookup"><span data-stu-id="e305d-113">EXAMPLES</span></span>

### <span data-ttu-id="e305d-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="e305d-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="e305d-115">此命令會取消註冊伺服器，導致此伺服器上所有伺服器端點的串聯刪除。</span><span class="sxs-lookup"><span data-stu-id="e305d-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="e305d-116">參數</span><span class="sxs-lookup"><span data-stu-id="e305d-116">PARAMETERS</span></span>

### <span data-ttu-id="e305d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e305d-117">-AsJob</span></span>
<span data-ttu-id="e305d-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e305d-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e305d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e305d-119">-DefaultProfile</span></span>
<span data-ttu-id="e305d-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e305d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e305d-121">-強制</span><span class="sxs-lookup"><span data-stu-id="e305d-121">-Force</span></span>
<span data-ttu-id="e305d-122">提供 -強制跳過此命令的確認。</span><span class="sxs-lookup"><span data-stu-id="e305d-122">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="e305d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e305d-123">-InputObject</span></span>
<span data-ttu-id="e305d-124">RegisteredServer 輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="e305d-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e305d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e305d-125">-PassThru</span></span>
<span data-ttu-id="e305d-126">在一般執行中，此 Cmdlet 不會在成功時獲得任何值。</span><span class="sxs-lookup"><span data-stu-id="e305d-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="e305d-127">如果您提供 PassThru 參數，則成功執行之後，Cmdlet 會寫入值至管線。</span><span class="sxs-lookup"><span data-stu-id="e305d-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="e305d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e305d-128">-ResourceGroupName</span></span>
<span data-ttu-id="e305d-129">資源組名。</span><span class="sxs-lookup"><span data-stu-id="e305d-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="e305d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e305d-130">-ResourceId</span></span>
<span data-ttu-id="e305d-131">RegisteredServer 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e305d-131">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="e305d-132">-ServerId</span><span class="sxs-lookup"><span data-stu-id="e305d-132">-ServerId</span></span>
<span data-ttu-id="e305d-133">RegisteredServer 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e305d-133">Name of the RegisteredServer.</span></span>

```yaml
Type: System.Guid
Parameter Sets: StringParameterSet
Aliases: RegisteredServerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e305d-134">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="e305d-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="e305d-135">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e305d-135">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e305d-136">-確認</span><span class="sxs-lookup"><span data-stu-id="e305d-136">-Confirm</span></span>
<span data-ttu-id="e305d-137">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e305d-137">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e305d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e305d-138">-WhatIf</span></span>
<span data-ttu-id="e305d-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e305d-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e305d-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e305d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e305d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e305d-141">CommonParameters</span></span>
<span data-ttu-id="e305d-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e305d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e305d-143">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e305d-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e305d-144">輸入</span><span class="sxs-lookup"><span data-stu-id="e305d-144">INPUTS</span></span>

### <span data-ttu-id="e305d-145">Microsoft.Azure.Commands.StorageSync.models.PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="e305d-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="e305d-146">System.String</span><span class="sxs-lookup"><span data-stu-id="e305d-146">System.String</span></span>

### <span data-ttu-id="e305d-147">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e305d-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e305d-148">輸出</span><span class="sxs-lookup"><span data-stu-id="e305d-148">OUTPUTS</span></span>

### <span data-ttu-id="e305d-149">System.Object</span><span class="sxs-lookup"><span data-stu-id="e305d-149">System.Object</span></span>
## <span data-ttu-id="e305d-150">筆記</span><span class="sxs-lookup"><span data-stu-id="e305d-150">NOTES</span></span>

## <span data-ttu-id="e305d-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="e305d-151">RELATED LINKS</span></span>
