---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 719ca5b8b837523359f4d55209956f7c68c3c93f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912233"
---
# <span data-ttu-id="11d02-101">Set-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="11d02-101">Set-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="11d02-102">簡介</span><span class="sxs-lookup"><span data-stu-id="11d02-102">SYNOPSIS</span></span>
<span data-ttu-id="11d02-103">為 Synapse Analytics SQL 資料庫提供 Azure AD 系統管理員。</span><span class="sxs-lookup"><span data-stu-id="11d02-103">Provisions an Azure AD administrator for Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="11d02-104">語法</span><span class="sxs-lookup"><span data-stu-id="11d02-104">SYNTAX</span></span>

### <span data-ttu-id="11d02-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="11d02-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 -DisplayName <String> [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11d02-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11d02-106">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace> -DisplayName <String>
 [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11d02-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11d02-107">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> -DisplayName <String> [-ObjectId <Guid>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11d02-108">描述</span><span class="sxs-lookup"><span data-stu-id="11d02-108">DESCRIPTION</span></span>
<span data-ttu-id="11d02-109">**Set-AzSynapseSqlActiveDirectoryAdministrator** Cmdlet 會針對目前訂閱中的 Azure Synapse Analytics Workspace 提供 Azure Active Directory (Azure AD) 系統管理員。</span><span class="sxs-lookup"><span data-stu-id="11d02-109">The **Set-AzSynapseSqlActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for Azure Synapse Analytics Workspace in the current subscription.</span></span>
<span data-ttu-id="11d02-110">您一次只能配置一位系統管理員。</span><span class="sxs-lookup"><span data-stu-id="11d02-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="11d02-111">下列 Azure AD 成員可以作為 Synapse Analytics Workspace 系統管理員進行設置：</span><span class="sxs-lookup"><span data-stu-id="11d02-111">The following members of Azure AD can be provisioned as a Synapse Analytics Workspace administrator:</span></span>
- <span data-ttu-id="11d02-112">Azure AD 的原生成員</span><span class="sxs-lookup"><span data-stu-id="11d02-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="11d02-113">Azure AD 的聯盟成員</span><span class="sxs-lookup"><span data-stu-id="11d02-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="11d02-114">從原生或聯盟成員的其他 Azure AD 中匯出成員</span><span class="sxs-lookup"><span data-stu-id="11d02-114">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="11d02-115">系統管理員不支援以安全性群組方式建立 Azure AD 群組的 Microsoft 帳戶，例如 Outlook.com、Hotmail.com 或 Live.com 網域中的帳戶。</span><span class="sxs-lookup"><span data-stu-id="11d02-115">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="11d02-116">系統管理員不支援其他來賓帳戶，例如 Gmail.com或Yahoo.com中的來賓帳戶。</span><span class="sxs-lookup"><span data-stu-id="11d02-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="11d02-117">建議您以系統管理員的名將專用 Azure AD 群組進行設置。</span><span class="sxs-lookup"><span data-stu-id="11d02-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="11d02-118">例子</span><span class="sxs-lookup"><span data-stu-id="11d02-118">EXAMPLES</span></span>

### <span data-ttu-id="11d02-119">範例 1</span><span class="sxs-lookup"><span data-stu-id="11d02-119">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs"
```

<span data-ttu-id="11d02-120">此命令會為名為 ContosoWorkspace 的工作區布布名為 DBAs 的 Azure AD 系統管理員群組。</span><span class="sxs-lookup"><span data-stu-id="11d02-120">This command provisions an Azure AD administrator group named DBAs for the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="11d02-121">範例 2</span><span class="sxs-lookup"><span data-stu-id="11d02-121">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
```

<span data-ttu-id="11d02-122">此命令會為名為 ContosoWorkspace 的工作區布布名為 DBAs 的 Azure AD 系統管理員群組。</span><span class="sxs-lookup"><span data-stu-id="11d02-122">This command provisions an Azure AD administrator group named DBAs for the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="11d02-123">這樣即使群組的顯示名稱並非唯一，也能夠確保命令成功。</span><span class="sxs-lookup"><span data-stu-id="11d02-123">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="11d02-124">參數</span><span class="sxs-lookup"><span data-stu-id="11d02-124">PARAMETERS</span></span>

### <span data-ttu-id="11d02-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11d02-125">-AsJob</span></span>
<span data-ttu-id="11d02-126">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="11d02-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11d02-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11d02-127">-DefaultProfile</span></span>
<span data-ttu-id="11d02-128">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="11d02-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11d02-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="11d02-129">-DisplayName</span></span>
<span data-ttu-id="11d02-130">指定要授予許可權的使用者或群組的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="11d02-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="11d02-131">此顯示名稱必須存在於與目前訂閱相關聯的 Active Directory 中。</span><span class="sxs-lookup"><span data-stu-id="11d02-131">This display name must exist in the active directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="11d02-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11d02-132">-InputObject</span></span>
<span data-ttu-id="11d02-133">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="11d02-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="11d02-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="11d02-134">-ObjectId</span></span>
<span data-ttu-id="11d02-135">指定 Azure Active Directory 中使用者或群組的物件識別碼，以授予許可權。</span><span class="sxs-lookup"><span data-stu-id="11d02-135">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

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

### <span data-ttu-id="11d02-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11d02-136">-ResourceGroupName</span></span>
<span data-ttu-id="11d02-137">資源組名。</span><span class="sxs-lookup"><span data-stu-id="11d02-137">Resource group name.</span></span>

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

### <span data-ttu-id="11d02-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11d02-138">-ResourceId</span></span>
<span data-ttu-id="11d02-139">Synapse 工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="11d02-139">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="11d02-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="11d02-140">-WorkspaceName</span></span>
<span data-ttu-id="11d02-141">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="11d02-141">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="11d02-142">-確認</span><span class="sxs-lookup"><span data-stu-id="11d02-142">-Confirm</span></span>
<span data-ttu-id="11d02-143">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="11d02-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11d02-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11d02-144">-WhatIf</span></span>
<span data-ttu-id="11d02-145">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="11d02-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11d02-146">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11d02-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11d02-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11d02-147">CommonParameters</span></span>
<span data-ttu-id="11d02-148">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="11d02-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11d02-149">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11d02-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11d02-150">輸入</span><span class="sxs-lookup"><span data-stu-id="11d02-150">INPUTS</span></span>

### <span data-ttu-id="11d02-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="11d02-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="11d02-152">輸出</span><span class="sxs-lookup"><span data-stu-id="11d02-152">OUTPUTS</span></span>

### <span data-ttu-id="11d02-153">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span><span class="sxs-lookup"><span data-stu-id="11d02-153">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span></span>

## <span data-ttu-id="11d02-154">筆記</span><span class="sxs-lookup"><span data-stu-id="11d02-154">NOTES</span></span>

## <span data-ttu-id="11d02-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="11d02-155">RELATED LINKS</span></span>
