---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: 87734d63d28785282ad3285ef8cce0a574ba30e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614410"
---
# <span data-ttu-id="94aaf-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="94aaf-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="94aaf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="94aaf-102">SYNOPSIS</span></span>
<span data-ttu-id="94aaf-103">警告：取消註冊伺服器會導致層疊刪除此伺服器上的所有伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="94aaf-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="94aaf-104">這個命令會登出伺服器的儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="94aaf-104">This command will unregister a server it's the storage sync service.</span></span>

## <span data-ttu-id="94aaf-105">句法</span><span class="sxs-lookup"><span data-stu-id="94aaf-105">SYNTAX</span></span>

### <span data-ttu-id="94aaf-106">InputObjectParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="94aaf-106">InputObjectParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94aaf-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94aaf-107">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94aaf-108">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="94aaf-108">StringParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94aaf-109">說明</span><span class="sxs-lookup"><span data-stu-id="94aaf-109">DESCRIPTION</span></span>
<span data-ttu-id="94aaf-110">這個命令會從儲存同步處理服務登出伺服器。</span><span class="sxs-lookup"><span data-stu-id="94aaf-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="94aaf-111">警告：取消註冊伺服器會導致層疊刪除此伺服器上的所有伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="94aaf-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="94aaf-112">只有在您確定此伺服器上的任何路徑都要再同步處理時，才應呼叫它。</span><span class="sxs-lookup"><span data-stu-id="94aaf-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="94aaf-113">示例</span><span class="sxs-lookup"><span data-stu-id="94aaf-113">EXAMPLES</span></span>

### <span data-ttu-id="94aaf-114">範例1</span><span class="sxs-lookup"><span data-stu-id="94aaf-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="94aaf-115">這個命令會登出伺服器，導致此伺服器上所有伺服器端點的串聯刪除。</span><span class="sxs-lookup"><span data-stu-id="94aaf-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="94aaf-116">參數</span><span class="sxs-lookup"><span data-stu-id="94aaf-116">PARAMETERS</span></span>

### <span data-ttu-id="94aaf-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94aaf-117">-AsJob</span></span>
<span data-ttu-id="94aaf-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="94aaf-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94aaf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94aaf-119">-DefaultProfile</span></span>
<span data-ttu-id="94aaf-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="94aaf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94aaf-121">-Force</span><span class="sxs-lookup"><span data-stu-id="94aaf-121">-Force</span></span>
<span data-ttu-id="94aaf-122">[提供-強制略過此命令的確認]。</span><span class="sxs-lookup"><span data-stu-id="94aaf-122">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="94aaf-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94aaf-123">-InputObject</span></span>
<span data-ttu-id="94aaf-124">RegisteredServer 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="94aaf-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="94aaf-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94aaf-125">-PassThru</span></span>
<span data-ttu-id="94aaf-126">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="94aaf-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="94aaf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94aaf-127">-ResourceGroupName</span></span>
<span data-ttu-id="94aaf-128">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="94aaf-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="94aaf-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94aaf-129">-ResourceId</span></span>
<span data-ttu-id="94aaf-130">RegisteredServer 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="94aaf-130">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="94aaf-131">-ServerId</span><span class="sxs-lookup"><span data-stu-id="94aaf-131">-ServerId</span></span>
<span data-ttu-id="94aaf-132">RegisteredServer 的名稱。</span><span class="sxs-lookup"><span data-stu-id="94aaf-132">Name of the RegisteredServer.</span></span>

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

### <span data-ttu-id="94aaf-133">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="94aaf-133">-StorageSyncServiceName</span></span>
<span data-ttu-id="94aaf-134">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="94aaf-134">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="94aaf-135">-確認</span><span class="sxs-lookup"><span data-stu-id="94aaf-135">-Confirm</span></span>
<span data-ttu-id="94aaf-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="94aaf-136">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94aaf-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94aaf-137">-WhatIf</span></span>
<span data-ttu-id="94aaf-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="94aaf-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94aaf-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94aaf-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94aaf-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94aaf-140">CommonParameters</span></span>
<span data-ttu-id="94aaf-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="94aaf-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94aaf-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="94aaf-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94aaf-143">輸入</span><span class="sxs-lookup"><span data-stu-id="94aaf-143">INPUTS</span></span>

### <span data-ttu-id="94aaf-144">PSRegisteredServer 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="94aaf-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="94aaf-145">System.object</span><span class="sxs-lookup"><span data-stu-id="94aaf-145">System.String</span></span>

### <span data-ttu-id="94aaf-146">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="94aaf-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="94aaf-147">輸出</span><span class="sxs-lookup"><span data-stu-id="94aaf-147">OUTPUTS</span></span>

### <span data-ttu-id="94aaf-148">System.object</span><span class="sxs-lookup"><span data-stu-id="94aaf-148">System.Object</span></span>
## <span data-ttu-id="94aaf-149">筆記</span><span class="sxs-lookup"><span data-stu-id="94aaf-149">NOTES</span></span>

## <span data-ttu-id="94aaf-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="94aaf-150">RELATED LINKS</span></span>
