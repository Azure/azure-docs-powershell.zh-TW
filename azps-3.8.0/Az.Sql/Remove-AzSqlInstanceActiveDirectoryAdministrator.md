---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 361517912166c9548ecc69358c6dd0e776cfcd3a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958696"
---
# <span data-ttu-id="88ea8-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="88ea8-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="88ea8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="88ea8-102">SYNOPSIS</span></span>
<span data-ttu-id="88ea8-103">移除 SQL 管理實例的 Azure AD 管理員。</span><span class="sxs-lookup"><span data-stu-id="88ea8-103">Removes an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="88ea8-104">句法</span><span class="sxs-lookup"><span data-stu-id="88ea8-104">SYNTAX</span></span>

### <span data-ttu-id="88ea8-105">UseResourceGroupAndInstanceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="88ea8-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88ea8-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88ea8-106">UseInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru]
 -InputObject <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88ea8-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88ea8-107">UserResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88ea8-108">說明</span><span class="sxs-lookup"><span data-stu-id="88ea8-108">DESCRIPTION</span></span>
<span data-ttu-id="88ea8-109">**AzSqlInstanceActiveDirectoryAdministrator** Cmdlet 會將 Azure Active Directory (azure AD) 管理員在目前的訂閱中移除 AzureSQL Managed 實例。</span><span class="sxs-lookup"><span data-stu-id="88ea8-109">The **Remove-AzSqlInstanceActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="88ea8-110">示例</span><span class="sxs-lookup"><span data-stu-id="88ea8-110">EXAMPLES</span></span>

### <span data-ttu-id="88ea8-111">範例1：移除系統管理員</span><span class="sxs-lookup"><span data-stu-id="88ea8-111">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstanceName01" -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="88ea8-112">這個命令會移除與資源群組 ResourceGroup01 相關聯之受管理實例的 Azure AD 系統管理員（名為 ManagedInstanceName01）。</span><span class="sxs-lookup"><span data-stu-id="88ea8-112">This command removes the Azure AD administrator for the managed instance named ManagedInstanceName01 associated with the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="88ea8-113">範例2</span><span class="sxs-lookup"><span data-stu-id="88ea8-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="88ea8-114">此命令會從 managed 實例物件中移除 Azure AD 系統管理員。</span><span class="sxs-lookup"><span data-stu-id="88ea8-114">This command removes the Azure AD administrator from the managed instance object.</span></span>

### <span data-ttu-id="88ea8-115">範例3</span><span class="sxs-lookup"><span data-stu-id="88ea8-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="88ea8-116">這個命令會使用受管理的實例資源識別碼來移除 Azure AD 系統管理員。</span><span class="sxs-lookup"><span data-stu-id="88ea8-116">This command removes the Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="88ea8-117">參數</span><span class="sxs-lookup"><span data-stu-id="88ea8-117">PARAMETERS</span></span>

### <span data-ttu-id="88ea8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88ea8-118">-DefaultProfile</span></span>
<span data-ttu-id="88ea8-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="88ea8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88ea8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="88ea8-120">-Force</span></span>
<span data-ttu-id="88ea8-121">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="88ea8-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="88ea8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88ea8-122">-InputObject</span></span>
<span data-ttu-id="88ea8-123">要使用的 managed 實例物件。</span><span class="sxs-lookup"><span data-stu-id="88ea8-123">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88ea8-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="88ea8-124">-InstanceName</span></span>
<span data-ttu-id="88ea8-125">SQL Managed 實例名稱。</span><span class="sxs-lookup"><span data-stu-id="88ea8-125">SQL Managed Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ea8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88ea8-126">-PassThru</span></span>
<span data-ttu-id="88ea8-127">定義是否要傳回已移除的 AD 系統管理員</span><span class="sxs-lookup"><span data-stu-id="88ea8-127">Defines whether to return the removed AD administrator</span></span>

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

### <span data-ttu-id="88ea8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88ea8-128">-ResourceGroupName</span></span>
<span data-ttu-id="88ea8-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="88ea8-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ea8-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88ea8-130">-ResourceId</span></span>
<span data-ttu-id="88ea8-131">要使用之實例的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="88ea8-131">The resource id of instance to use</span></span>

```yaml
Type: System.String
Parameter Sets: UserResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ea8-132">-確認</span><span class="sxs-lookup"><span data-stu-id="88ea8-132">-Confirm</span></span>
<span data-ttu-id="88ea8-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="88ea8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88ea8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88ea8-134">-WhatIf</span></span>
<span data-ttu-id="88ea8-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="88ea8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88ea8-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="88ea8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88ea8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88ea8-137">CommonParameters</span></span>
<span data-ttu-id="88ea8-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="88ea8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88ea8-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="88ea8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88ea8-140">輸入</span><span class="sxs-lookup"><span data-stu-id="88ea8-140">INPUTS</span></span>

### <span data-ttu-id="88ea8-141">System.object</span><span class="sxs-lookup"><span data-stu-id="88ea8-141">System.String</span></span>

## <span data-ttu-id="88ea8-142">輸出</span><span class="sxs-lookup"><span data-stu-id="88ea8-142">OUTPUTS</span></span>

### <span data-ttu-id="88ea8-143">AzureSqlInstanceActiveDirectoryAdministratorModel 中的 [InstanceActiveDirectoryAdministrator]</span><span class="sxs-lookup"><span data-stu-id="88ea8-143">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="88ea8-144">筆記</span><span class="sxs-lookup"><span data-stu-id="88ea8-144">NOTES</span></span>

## <span data-ttu-id="88ea8-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="88ea8-145">RELATED LINKS</span></span>

[<span data-ttu-id="88ea8-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="88ea8-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="88ea8-147">AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="88ea8-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)
