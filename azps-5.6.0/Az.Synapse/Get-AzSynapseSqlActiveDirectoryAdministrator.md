---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 1f5c9c619c037c243246f9dec26ae2504a162d9b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917853"
---
# <span data-ttu-id="f2f54-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f2f54-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="f2f54-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f2f54-102">SYNOPSIS</span></span>
<span data-ttu-id="f2f54-103">獲得 Synapse Analytics Workspace 的 Azure AD 系統管理員相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f2f54-103">Gets information about an Azure AD administrator for Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="f2f54-104">語法</span><span class="sxs-lookup"><span data-stu-id="f2f54-104">SYNTAX</span></span>

### <span data-ttu-id="f2f54-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f2f54-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2f54-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2f54-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2f54-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2f54-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2f54-108">描述</span><span class="sxs-lookup"><span data-stu-id="f2f54-108">DESCRIPTION</span></span>
<span data-ttu-id="f2f54-109">**Get-AzSynapseSqlActiveDirectoryAdministrator** Cmdlet 會取得目前訂閱中 Azure Synapse Analytics Workspace 的 Azure Active Directory (Azure AD) 系統管理員相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f2f54-109">The **Get-AzSynapseSqlActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an Azure Synapse Analytics Workspace in the current subscription.</span></span>

## <span data-ttu-id="f2f54-110">例子</span><span class="sxs-lookup"><span data-stu-id="f2f54-110">EXAMPLES</span></span>

### <span data-ttu-id="f2f54-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="f2f54-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="f2f54-112">此命令會針對名為 ContosoWorkspace 的工作區，獲得 Azure AD 系統管理員的資訊。</span><span class="sxs-lookup"><span data-stu-id="f2f54-112">This command gets information about an Azure AD administrator for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="f2f54-113">參數</span><span class="sxs-lookup"><span data-stu-id="f2f54-113">PARAMETERS</span></span>

### <span data-ttu-id="f2f54-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2f54-114">-DefaultProfile</span></span>
<span data-ttu-id="f2f54-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2f54-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2f54-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2f54-116">-InputObject</span></span>
<span data-ttu-id="f2f54-117">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="f2f54-117">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f2f54-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2f54-118">-ResourceGroupName</span></span>
<span data-ttu-id="f2f54-119">資源組名。</span><span class="sxs-lookup"><span data-stu-id="f2f54-119">Resource group name.</span></span>

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

### <span data-ttu-id="f2f54-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2f54-120">-ResourceId</span></span>
<span data-ttu-id="f2f54-121">Synapse 工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f2f54-121">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="f2f54-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f2f54-122">-WorkspaceName</span></span>
<span data-ttu-id="f2f54-123">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2f54-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f2f54-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2f54-124">CommonParameters</span></span>
<span data-ttu-id="f2f54-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f2f54-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2f54-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2f54-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2f54-127">輸入</span><span class="sxs-lookup"><span data-stu-id="f2f54-127">INPUTS</span></span>

### <span data-ttu-id="f2f54-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f2f54-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f2f54-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f2f54-129">OUTPUTS</span></span>

### <span data-ttu-id="f2f54-130">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span><span class="sxs-lookup"><span data-stu-id="f2f54-130">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span></span>

## <span data-ttu-id="f2f54-131">筆記</span><span class="sxs-lookup"><span data-stu-id="f2f54-131">NOTES</span></span>

## <span data-ttu-id="f2f54-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2f54-132">RELATED LINKS</span></span>
