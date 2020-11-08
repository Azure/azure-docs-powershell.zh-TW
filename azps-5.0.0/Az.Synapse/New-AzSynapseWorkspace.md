---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
ms.openlocfilehash: fb3613555e65b0d13650e5c15189edd865ab2b89
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140737"
---
# <span data-ttu-id="8360a-101">New-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8360a-101">New-AzSynapseWorkspace</span></span>

## <span data-ttu-id="8360a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8360a-102">SYNOPSIS</span></span>
<span data-ttu-id="8360a-103">建立 Synapse 分析工作區。</span><span class="sxs-lookup"><span data-stu-id="8360a-103">Creates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="8360a-104">句法</span><span class="sxs-lookup"><span data-stu-id="8360a-104">SYNTAX</span></span>

```
New-AzSynapseWorkspace -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 -DefaultDataLakeStorageAccountName <String> -DefaultDataLakeStorageFilesystem <String>
 -SqlAdministratorLoginCredential <PSCredential> [-ManagedVirtualNetwork <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8360a-105">說明</span><span class="sxs-lookup"><span data-stu-id="8360a-105">DESCRIPTION</span></span>
<span data-ttu-id="8360a-106">**新的-AzSynapseWorkspace** Cmdlet 會建立 Azure Synapse 分析工作區。</span><span class="sxs-lookup"><span data-stu-id="8360a-106">The **New-AzSynapseWorkspace** cmdlet creates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="8360a-107">示例</span><span class="sxs-lookup"><span data-stu-id="8360a-107">EXAMPLES</span></span>

### <span data-ttu-id="8360a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="8360a-108">Example 1</span></span>
```powershell
PS C:\> $password = ConvertTo-SecureString "Password123!" -AsPlainText -Force
PS C:\> $creds = New-Object System.Management.Automation.PSCredential ("ContosoUser", $password)
PS C:\> New-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -Name ContosoWorkspace -Location northeurope -DefaultDataLakeStorageAccountName ContosoAdlGen2Storage -DefaultDataLakeStorageFilesystem ContosoFileSystem -SqlAdministratorLoginCredential $creds -AsJob
```

<span data-ttu-id="8360a-109">這個命令會在名為 ContosoResourceGroup 的資源群組中，建立一個名為 ContosoWorkspace 的 Synapse 分析工作區，該工作區使用 ContosoAdlGenStorage 資料存放區。</span><span class="sxs-lookup"><span data-stu-id="8360a-109">This command creates a Synapse Analytics workspace named ContosoWorkspace that uses the ContosoAdlGenStorage Data Store, in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="8360a-110">參數</span><span class="sxs-lookup"><span data-stu-id="8360a-110">PARAMETERS</span></span>

### <span data-ttu-id="8360a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8360a-111">-AsJob</span></span>
<span data-ttu-id="8360a-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8360a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8360a-113">-DefaultDataLakeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8360a-113">-DefaultDataLakeStorageAccountName</span></span>
<span data-ttu-id="8360a-114">預設的 ADLS Gen2 儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="8360a-114">The default ADLS Gen2 storage account name.</span></span>

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

### <span data-ttu-id="8360a-115">-DefaultDataLakeStorageFilesystem</span><span class="sxs-lookup"><span data-stu-id="8360a-115">-DefaultDataLakeStorageFilesystem</span></span>
<span data-ttu-id="8360a-116">預設的 ADLS Gen2 檔案系統。</span><span class="sxs-lookup"><span data-stu-id="8360a-116">The default ADLS Gen2 file system.</span></span>

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

### <span data-ttu-id="8360a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8360a-117">-DefaultProfile</span></span>
<span data-ttu-id="8360a-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8360a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8360a-119">-位置</span><span class="sxs-lookup"><span data-stu-id="8360a-119">-Location</span></span>
<span data-ttu-id="8360a-120">應建立資源的 Azure 地區。</span><span class="sxs-lookup"><span data-stu-id="8360a-120">Azure region where the resource should be created.</span></span>

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

### <span data-ttu-id="8360a-121">-ManagedVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8360a-121">-ManagedVirtualNetwork</span></span>
<span data-ttu-id="8360a-122">專用於 Azure Synapse 工作區的 Synapse 管理虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="8360a-122">Name of a Synapse-managed virtual network dedicated for the Azure Synapse workspace.</span></span>

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

### <span data-ttu-id="8360a-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="8360a-123">-Name</span></span>
<span data-ttu-id="8360a-124">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="8360a-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8360a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8360a-125">-ResourceGroupName</span></span>
<span data-ttu-id="8360a-126">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8360a-126">Resource group name.</span></span>

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

### <span data-ttu-id="8360a-127">-SqlAdministratorLoginCredential</span><span class="sxs-lookup"><span data-stu-id="8360a-127">-SqlAdministratorLoginCredential</span></span>
<span data-ttu-id="8360a-128">SQL 系統管理員認證。</span><span class="sxs-lookup"><span data-stu-id="8360a-128">SQL administrator credentials.</span></span>

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

### <span data-ttu-id="8360a-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="8360a-129">-Tag</span></span>
<span data-ttu-id="8360a-130">與資源相關聯之標記的字串字典。</span><span class="sxs-lookup"><span data-stu-id="8360a-130">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="8360a-131">-確認</span><span class="sxs-lookup"><span data-stu-id="8360a-131">-Confirm</span></span>
<span data-ttu-id="8360a-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8360a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8360a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8360a-133">-WhatIf</span></span>
<span data-ttu-id="8360a-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8360a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8360a-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8360a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8360a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8360a-136">CommonParameters</span></span>
<span data-ttu-id="8360a-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8360a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8360a-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8360a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8360a-139">輸入</span><span class="sxs-lookup"><span data-stu-id="8360a-139">INPUTS</span></span>

### <span data-ttu-id="8360a-140">System.object</span><span class="sxs-lookup"><span data-stu-id="8360a-140">System.String</span></span>

### <span data-ttu-id="8360a-141">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8360a-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8360a-142">系統管理. PSCredential</span><span class="sxs-lookup"><span data-stu-id="8360a-142">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="8360a-143">輸出</span><span class="sxs-lookup"><span data-stu-id="8360a-143">OUTPUTS</span></span>

### <span data-ttu-id="8360a-144">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="8360a-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="8360a-145">筆記</span><span class="sxs-lookup"><span data-stu-id="8360a-145">NOTES</span></span>

## <span data-ttu-id="8360a-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="8360a-146">RELATED LINKS</span></span>
