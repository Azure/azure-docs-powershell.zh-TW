---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
ms.openlocfilehash: 28f1486375e0efc1f9b1b3f9a18f12050dafd799
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914989"
---
# <span data-ttu-id="0201c-101">New-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0201c-101">New-AzSynapseWorkspace</span></span>

## <span data-ttu-id="0201c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0201c-102">SYNOPSIS</span></span>
<span data-ttu-id="0201c-103">建立 Synapse Analytics 工作區。</span><span class="sxs-lookup"><span data-stu-id="0201c-103">Creates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="0201c-104">語法</span><span class="sxs-lookup"><span data-stu-id="0201c-104">SYNTAX</span></span>

```
New-AzSynapseWorkspace -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 -DefaultDataLakeStorageAccountName <String> -DefaultDataLakeStorageFilesystem <String>
 -SqlAdministratorLoginCredential <PSCredential> [-ManagedVirtualNetwork <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0201c-105">描述</span><span class="sxs-lookup"><span data-stu-id="0201c-105">DESCRIPTION</span></span>
<span data-ttu-id="0201c-106">**New-AzSynapseWorkspace** Cmdlet 會建立 Azure Synapse Analytics 工作區。</span><span class="sxs-lookup"><span data-stu-id="0201c-106">The **New-AzSynapseWorkspace** cmdlet creates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="0201c-107">例子</span><span class="sxs-lookup"><span data-stu-id="0201c-107">EXAMPLES</span></span>

### <span data-ttu-id="0201c-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="0201c-108">Example 1</span></span>
```powershell
PS C:\> $password = ConvertTo-SecureString "Password123!" -AsPlainText -Force
PS C:\> $creds = New-Object System.Management.Automation.PSCredential ("ContosoUser", $password)
PS C:\> New-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -Name ContosoWorkspace -Location northeurope -DefaultDataLakeStorageAccountName ContosoAdlGen2Storage -DefaultDataLakeStorageFilesystem ContosoFileSystem -SqlAdministratorLoginCredential $creds -AsJob
```

<span data-ttu-id="0201c-109">此命令會建立名為 ContosoWorkspace 的 Synapse Analytics 工作區，該工作區使用名為 ContosoAdlGenStorage Data Store 的資源群組 ContosoResourceGroup。</span><span class="sxs-lookup"><span data-stu-id="0201c-109">This command creates a Synapse Analytics workspace named ContosoWorkspace that uses the ContosoAdlGenStorage Data Store, in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="0201c-110">參數</span><span class="sxs-lookup"><span data-stu-id="0201c-110">PARAMETERS</span></span>

### <span data-ttu-id="0201c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0201c-111">-AsJob</span></span>
<span data-ttu-id="0201c-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0201c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0201c-113">-DefaultDataLakeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0201c-113">-DefaultDataLakeStorageAccountName</span></span>
<span data-ttu-id="0201c-114">預設的 ADLS Gen2 儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="0201c-114">The default ADLS Gen2 storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0201c-115">-DefaultDataLakeStorageFilesystem</span><span class="sxs-lookup"><span data-stu-id="0201c-115">-DefaultDataLakeStorageFilesystem</span></span>
<span data-ttu-id="0201c-116">預設的 ADLS Gen2 檔案系統。</span><span class="sxs-lookup"><span data-stu-id="0201c-116">The default ADLS Gen2 file system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0201c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0201c-117">-DefaultProfile</span></span>
<span data-ttu-id="0201c-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0201c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0201c-119">-位置</span><span class="sxs-lookup"><span data-stu-id="0201c-119">-Location</span></span>
<span data-ttu-id="0201c-120">應建立資源的 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="0201c-120">Azure region where the resource should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0201c-121">-ManagedVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0201c-121">-ManagedVirtualNetwork</span></span>
<span data-ttu-id="0201c-122">專屬於 Azure Synapse 工作區的 Synapse 受管理的虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="0201c-122">Name of a Synapse-managed virtual network dedicated for the Azure Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: default

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0201c-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="0201c-123">-Name</span></span>
<span data-ttu-id="0201c-124">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="0201c-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0201c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0201c-125">-ResourceGroupName</span></span>
<span data-ttu-id="0201c-126">資源組名。</span><span class="sxs-lookup"><span data-stu-id="0201c-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0201c-127">-SqlAdministratorLoginCredential</span><span class="sxs-lookup"><span data-stu-id="0201c-127">-SqlAdministratorLoginCredential</span></span>
<span data-ttu-id="0201c-128">SQL 系統管理員認證。</span><span class="sxs-lookup"><span data-stu-id="0201c-128">SQL administrator credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0201c-129">-標記</span><span class="sxs-lookup"><span data-stu-id="0201c-129">-Tag</span></span>
<span data-ttu-id="0201c-130">與資源關聯的標記字串字典。</span><span class="sxs-lookup"><span data-stu-id="0201c-130">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0201c-131">-確認</span><span class="sxs-lookup"><span data-stu-id="0201c-131">-Confirm</span></span>
<span data-ttu-id="0201c-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0201c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0201c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0201c-133">-WhatIf</span></span>
<span data-ttu-id="0201c-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0201c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0201c-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0201c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0201c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0201c-136">CommonParameters</span></span>
<span data-ttu-id="0201c-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0201c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0201c-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0201c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0201c-139">輸入</span><span class="sxs-lookup"><span data-stu-id="0201c-139">INPUTS</span></span>

### <span data-ttu-id="0201c-140">System.String</span><span class="sxs-lookup"><span data-stu-id="0201c-140">System.String</span></span>

### <span data-ttu-id="0201c-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0201c-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0201c-142">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="0201c-142">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="0201c-143">輸出</span><span class="sxs-lookup"><span data-stu-id="0201c-143">OUTPUTS</span></span>

### <span data-ttu-id="0201c-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0201c-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="0201c-145">筆記</span><span class="sxs-lookup"><span data-stu-id="0201c-145">NOTES</span></span>

## <span data-ttu-id="0201c-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="0201c-146">RELATED LINKS</span></span>
