---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: f6de2bf731bc11a4b0ec8b6c894e6d77569ec9ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130547"
---
# <span data-ttu-id="367b9-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="367b9-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="367b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="367b9-102">SYNOPSIS</span></span>
<span data-ttu-id="367b9-103">警告：取消註冊伺服器會導致層疊刪除此伺服器上的所有伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="367b9-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="367b9-104">這個命令會從它的儲存同步處理服務登出伺服器。</span><span class="sxs-lookup"><span data-stu-id="367b9-104">This command will unregister a server from it's storage sync service.</span></span>

## <span data-ttu-id="367b9-105">句法</span><span class="sxs-lookup"><span data-stu-id="367b9-105">SYNTAX</span></span>

### <span data-ttu-id="367b9-106">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="367b9-106">StringParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="367b9-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="367b9-107">InputObjectParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="367b9-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="367b9-108">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="367b9-109">說明</span><span class="sxs-lookup"><span data-stu-id="367b9-109">DESCRIPTION</span></span>
<span data-ttu-id="367b9-110">這個命令會從儲存同步處理服務登出伺服器。</span><span class="sxs-lookup"><span data-stu-id="367b9-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="367b9-111">警告：取消註冊伺服器會導致層疊刪除此伺服器上的所有伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="367b9-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="367b9-112">只有在您確定此伺服器上的任何路徑都要再同步處理時，才應呼叫它。</span><span class="sxs-lookup"><span data-stu-id="367b9-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="367b9-113">示例</span><span class="sxs-lookup"><span data-stu-id="367b9-113">EXAMPLES</span></span>

### <span data-ttu-id="367b9-114">範例1</span><span class="sxs-lookup"><span data-stu-id="367b9-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="367b9-115">這個命令會登出伺服器，導致此伺服器上所有伺服器端點的串聯刪除。</span><span class="sxs-lookup"><span data-stu-id="367b9-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="367b9-116">參數</span><span class="sxs-lookup"><span data-stu-id="367b9-116">PARAMETERS</span></span>

### <span data-ttu-id="367b9-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="367b9-117">-AsJob</span></span>
<span data-ttu-id="367b9-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="367b9-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="367b9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="367b9-119">-DefaultProfile</span></span>
<span data-ttu-id="367b9-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="367b9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="367b9-121">-Force</span><span class="sxs-lookup"><span data-stu-id="367b9-121">-Force</span></span>
<span data-ttu-id="367b9-122">[提供-強制略過此命令的確認]。</span><span class="sxs-lookup"><span data-stu-id="367b9-122">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="367b9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="367b9-123">-InputObject</span></span>
<span data-ttu-id="367b9-124">RegisteredServer 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="367b9-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="367b9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="367b9-125">-PassThru</span></span>
<span data-ttu-id="367b9-126">在正常執行中，此 Cmdlet 在成功時不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="367b9-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="367b9-127">如果您提供 PassThru 參數，則在成功執行之後，Cmdlet 會將值寫入管道。</span><span class="sxs-lookup"><span data-stu-id="367b9-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="367b9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="367b9-128">-ResourceGroupName</span></span>
<span data-ttu-id="367b9-129">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="367b9-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="367b9-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="367b9-130">-ResourceId</span></span>
<span data-ttu-id="367b9-131">RegisteredServer 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="367b9-131">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="367b9-132">-ServerId</span><span class="sxs-lookup"><span data-stu-id="367b9-132">-ServerId</span></span>
<span data-ttu-id="367b9-133">RegisteredServer 的名稱。</span><span class="sxs-lookup"><span data-stu-id="367b9-133">Name of the RegisteredServer.</span></span>

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

### <span data-ttu-id="367b9-134">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="367b9-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="367b9-135">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="367b9-135">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="367b9-136">-確認</span><span class="sxs-lookup"><span data-stu-id="367b9-136">-Confirm</span></span>
<span data-ttu-id="367b9-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="367b9-137">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="367b9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="367b9-138">-WhatIf</span></span>
<span data-ttu-id="367b9-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="367b9-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="367b9-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="367b9-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="367b9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="367b9-141">CommonParameters</span></span>
<span data-ttu-id="367b9-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="367b9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="367b9-143">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="367b9-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="367b9-144">輸入</span><span class="sxs-lookup"><span data-stu-id="367b9-144">INPUTS</span></span>

### <span data-ttu-id="367b9-145">PSRegisteredServer 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="367b9-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="367b9-146">System.object</span><span class="sxs-lookup"><span data-stu-id="367b9-146">System.String</span></span>

### <span data-ttu-id="367b9-147">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="367b9-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="367b9-148">輸出</span><span class="sxs-lookup"><span data-stu-id="367b9-148">OUTPUTS</span></span>

### <span data-ttu-id="367b9-149">System.object</span><span class="sxs-lookup"><span data-stu-id="367b9-149">System.Object</span></span>
## <span data-ttu-id="367b9-150">筆記</span><span class="sxs-lookup"><span data-stu-id="367b9-150">NOTES</span></span>

## <span data-ttu-id="367b9-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="367b9-151">RELATED LINKS</span></span>
