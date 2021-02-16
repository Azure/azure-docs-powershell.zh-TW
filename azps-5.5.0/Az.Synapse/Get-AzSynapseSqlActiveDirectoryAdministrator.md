---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: d3ea1a67d8afa15549c19d6099dc727aab43adc5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100137702"
---
# <span data-ttu-id="84319-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="84319-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="84319-102">摘要</span><span class="sxs-lookup"><span data-stu-id="84319-102">SYNOPSIS</span></span>
<span data-ttu-id="84319-103">取得 Synapse Analytics 工作區的 Azure AD 系統管理員的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="84319-103">Gets information about an Azure AD administrator for Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="84319-104">句法</span><span class="sxs-lookup"><span data-stu-id="84319-104">SYNTAX</span></span>

### <span data-ttu-id="84319-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="84319-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84319-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84319-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84319-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="84319-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="84319-108">說明</span><span class="sxs-lookup"><span data-stu-id="84319-108">DESCRIPTION</span></span>
<span data-ttu-id="84319-109">**AzSynapseSqlActiveDirectoryAdministrator** Cmdlet 會取得 Azure Active Directory (azure AD) 管理員的相關資訊，以便在目前的訂閱中使用 Azure Synapse 分析工作區。</span><span class="sxs-lookup"><span data-stu-id="84319-109">The **Get-AzSynapseSqlActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an Azure Synapse Analytics Workspace in the current subscription.</span></span>

## <span data-ttu-id="84319-110">示例</span><span class="sxs-lookup"><span data-stu-id="84319-110">EXAMPLES</span></span>

### <span data-ttu-id="84319-111">範例1</span><span class="sxs-lookup"><span data-stu-id="84319-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="84319-112">這個命令會針對名為 ContosoWorkspace 的工作區，取得 Azure AD 系統管理員的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="84319-112">This command gets information about an Azure AD administrator for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="84319-113">參數</span><span class="sxs-lookup"><span data-stu-id="84319-113">PARAMETERS</span></span>

### <span data-ttu-id="84319-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84319-114">-DefaultProfile</span></span>
<span data-ttu-id="84319-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="84319-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84319-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84319-116">-InputObject</span></span>
<span data-ttu-id="84319-117">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="84319-117">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84319-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84319-118">-ResourceGroupName</span></span>
<span data-ttu-id="84319-119">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="84319-119">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84319-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84319-120">-ResourceId</span></span>
<span data-ttu-id="84319-121">Synapse 工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="84319-121">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84319-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="84319-122">-WorkspaceName</span></span>
<span data-ttu-id="84319-123">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="84319-123">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84319-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84319-124">CommonParameters</span></span>
<span data-ttu-id="84319-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="84319-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84319-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="84319-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84319-127">輸入</span><span class="sxs-lookup"><span data-stu-id="84319-127">INPUTS</span></span>

### <span data-ttu-id="84319-128">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="84319-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="84319-129">輸出</span><span class="sxs-lookup"><span data-stu-id="84319-129">OUTPUTS</span></span>

### <span data-ttu-id="84319-130">PSWorkspaceAadAdminInfo 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="84319-130">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span></span>

## <span data-ttu-id="84319-131">筆記</span><span class="sxs-lookup"><span data-stu-id="84319-131">NOTES</span></span>

## <span data-ttu-id="84319-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="84319-132">RELATED LINKS</span></span>
