---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 4a2293384cdf2cf579458d05c112469d096bfd9a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438932"
---
# <span data-ttu-id="8e192-101">Set-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="8e192-101">Set-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="8e192-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8e192-102">SYNOPSIS</span></span>
<span data-ttu-id="8e192-103">為 Synapse Analytics SQL pool 置備 Azure AD 系統管理員。</span><span class="sxs-lookup"><span data-stu-id="8e192-103">Provisions an Azure AD administrator for Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="8e192-104">句法</span><span class="sxs-lookup"><span data-stu-id="8e192-104">SYNTAX</span></span>

### <span data-ttu-id="8e192-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8e192-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 -DisplayName <String> [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e192-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e192-106">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace> -DisplayName <String>
 [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e192-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e192-107">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> -DisplayName <String> [-ObjectId <Guid>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e192-108">說明</span><span class="sxs-lookup"><span data-stu-id="8e192-108">DESCRIPTION</span></span>
<span data-ttu-id="8e192-109">**AzSynapseSqlActiveDirectoryAdministrator** Cmdlet 會將 Azure Active Directory (azure AD) 管理員提供給目前訂閱中的 Azure Synapse 分析工作區。</span><span class="sxs-lookup"><span data-stu-id="8e192-109">The **Set-AzSynapseSqlActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for Azure Synapse Analytics Workspace in the current subscription.</span></span>
<span data-ttu-id="8e192-110">您一次只能提供一個系統管理員。</span><span class="sxs-lookup"><span data-stu-id="8e192-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="8e192-111">下列 Azure AD 的成員可設為 Synapse Analytics 工作區系統管理員：</span><span class="sxs-lookup"><span data-stu-id="8e192-111">The following members of Azure AD can be provisioned as a Synapse Analytics Workspace administrator:</span></span>
- <span data-ttu-id="8e192-112">Azure AD 的原生成員</span><span class="sxs-lookup"><span data-stu-id="8e192-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="8e192-113">Azure AD 的聯合成員</span><span class="sxs-lookup"><span data-stu-id="8e192-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="8e192-114">從其他屬於原生或同盟成員的 Azure 廣告匯入的成員</span><span class="sxs-lookup"><span data-stu-id="8e192-114">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="8e192-115">已建立為安全性群組的 Azure AD 群組（例如 Outlook.com、Hotmail.com 或 Live.com 網域中的帳戶）不受系統管理員支援。</span><span class="sxs-lookup"><span data-stu-id="8e192-115">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="8e192-116">其他來賓帳戶（例如 Gmail.com 或 Yahoo.com 網域中的帳戶）不受系統管理員支援。</span><span class="sxs-lookup"><span data-stu-id="8e192-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="8e192-117">我們建議您以系統管理員身分提供專用的 Azure AD 群組。</span><span class="sxs-lookup"><span data-stu-id="8e192-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="8e192-118">示例</span><span class="sxs-lookup"><span data-stu-id="8e192-118">EXAMPLES</span></span>

### <span data-ttu-id="8e192-119">範例1</span><span class="sxs-lookup"><span data-stu-id="8e192-119">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs"
```

<span data-ttu-id="8e192-120">這個命令會為名為 ContosoWorkspace 的工作區提供一個名為 Dba 的 Azure AD 管理員群組。</span><span class="sxs-lookup"><span data-stu-id="8e192-120">This command provisions an Azure AD administrator group named DBAs for the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="8e192-121">範例2</span><span class="sxs-lookup"><span data-stu-id="8e192-121">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
```

<span data-ttu-id="8e192-122">這個命令會為名為 ContosoWorkspace 的工作區提供一個名為 Dba 的 Azure AD 管理員群組。</span><span class="sxs-lookup"><span data-stu-id="8e192-122">This command provisions an Azure AD administrator group named DBAs for the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="8e192-123">這可確保即使群組的顯示名稱不是唯一的，命令也會成功。</span><span class="sxs-lookup"><span data-stu-id="8e192-123">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="8e192-124">參數</span><span class="sxs-lookup"><span data-stu-id="8e192-124">PARAMETERS</span></span>

### <span data-ttu-id="8e192-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e192-125">-AsJob</span></span>
<span data-ttu-id="8e192-126">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8e192-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e192-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e192-127">-DefaultProfile</span></span>
<span data-ttu-id="8e192-128">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8e192-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e192-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8e192-129">-DisplayName</span></span>
<span data-ttu-id="8e192-130">指定要授與許可權的使用者或群組的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="8e192-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="8e192-131">此顯示名稱必須存在於與目前訂閱相關聯的 active directory 中。</span><span class="sxs-lookup"><span data-stu-id="8e192-131">This display name must exist in the active directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="8e192-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e192-132">-InputObject</span></span>
<span data-ttu-id="8e192-133">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="8e192-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e192-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8e192-134">-ObjectId</span></span>
<span data-ttu-id="8e192-135">指定 Azure Active Directory 中要授與許可權的使用者或群組物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="8e192-135">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e192-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e192-136">-ResourceGroupName</span></span>
<span data-ttu-id="8e192-137">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8e192-137">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e192-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e192-138">-ResourceId</span></span>
<span data-ttu-id="8e192-139">Synapse 工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8e192-139">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e192-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8e192-140">-WorkspaceName</span></span>
<span data-ttu-id="8e192-141">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e192-141">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e192-142">-確認</span><span class="sxs-lookup"><span data-stu-id="8e192-142">-Confirm</span></span>
<span data-ttu-id="8e192-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8e192-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e192-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e192-144">-WhatIf</span></span>
<span data-ttu-id="8e192-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8e192-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e192-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e192-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e192-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e192-147">CommonParameters</span></span>
<span data-ttu-id="8e192-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8e192-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e192-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8e192-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e192-150">輸入</span><span class="sxs-lookup"><span data-stu-id="8e192-150">INPUTS</span></span>

### <span data-ttu-id="8e192-151">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="8e192-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="8e192-152">輸出</span><span class="sxs-lookup"><span data-stu-id="8e192-152">OUTPUTS</span></span>

### <span data-ttu-id="8e192-153">PSWorkspaceAadAdminInfo 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="8e192-153">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span></span>

## <span data-ttu-id="8e192-154">筆記</span><span class="sxs-lookup"><span data-stu-id="8e192-154">NOTES</span></span>

## <span data-ttu-id="8e192-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e192-155">RELATED LINKS</span></span>
