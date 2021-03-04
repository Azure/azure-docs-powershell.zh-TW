---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: a8c748e2d37dbb4759df27b56b37719bcbb2babf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917886"
---
# <span data-ttu-id="49e09-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="49e09-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="49e09-102">簡介</span><span class="sxs-lookup"><span data-stu-id="49e09-102">SYNOPSIS</span></span>
<span data-ttu-id="49e09-103">為 SQL Managed 實例提供 Azure AD 系統管理員。</span><span class="sxs-lookup"><span data-stu-id="49e09-103">Provisions an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="49e09-104">語法</span><span class="sxs-lookup"><span data-stu-id="49e09-104">SYNTAX</span></span>

### <span data-ttu-id="49e09-105">UseResourceGroupAndInstanceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="49e09-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49e09-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49e09-106">UseInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 -InputObject <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49e09-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49e09-107">UserResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49e09-108">描述</span><span class="sxs-lookup"><span data-stu-id="49e09-108">DESCRIPTION</span></span>
<span data-ttu-id="49e09-109">**Set-AzSqlInstanceActiveDirectoryAdministrator** Cmdlet 會針對目前訂閱中的 Azure Active Directory (Azure AD) 系統管理員，提供 Azure Active Directory (Azure AD) 系統管理員。</span><span class="sxs-lookup"><span data-stu-id="49e09-109">The **Set-AzSqlInstanceActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>
<span data-ttu-id="49e09-110">您一次只能配置一位系統管理員。</span><span class="sxs-lookup"><span data-stu-id="49e09-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="49e09-111">下列 Azure AD 成員可以作為 SQL Managed 實例系統管理員進行設置：</span><span class="sxs-lookup"><span data-stu-id="49e09-111">The following members of Azure AD can be provisioned as a SQL Managed Instance administrator:</span></span>
- <span data-ttu-id="49e09-112">Azure AD 的原生成員</span><span class="sxs-lookup"><span data-stu-id="49e09-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="49e09-113">Azure AD 的聯盟成員</span><span class="sxs-lookup"><span data-stu-id="49e09-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="49e09-114">系統管理員不支援從其他 Azure AD 將成員從其他 Azure AD 中匯出為安全性群組所建立之 Azure AD 群組。</span><span class="sxs-lookup"><span data-stu-id="49e09-114">Azure AD groups created as security groups Imported members from other Azure ADs are not supported as administrators.</span></span>
<span data-ttu-id="49e09-115">系統管理員不支援 Microsoft 帳戶，例如 Outlook.com、Hotmail.com 或 Live.com 中的帳戶。</span><span class="sxs-lookup"><span data-stu-id="49e09-115">Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="49e09-116">系統管理員不支援其他來賓帳戶，例如 Gmail.com或Yahoo.com中的來賓帳戶。</span><span class="sxs-lookup"><span data-stu-id="49e09-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="49e09-117">建議您以系統管理員的名將專用 Azure AD 群組進行設置。</span><span class="sxs-lookup"><span data-stu-id="49e09-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="49e09-118">例子</span><span class="sxs-lookup"><span data-stu-id="49e09-118">EXAMPLES</span></span>

### <span data-ttu-id="49e09-119">範例 1：為與資源群組相關聯的受管理實例提供系統管理員群組</span><span class="sxs-lookup"><span data-stu-id="49e09-119">Example 1: Provision an administrator group for a managed instance associated with resource group</span></span>
```
PS C:\>Set-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="49e09-120">此命令會為 ManagedInstance01 受管理實例提供名為 DBAs 的 Azure AD 系統管理員群組。</span><span class="sxs-lookup"><span data-stu-id="49e09-120">This command provisions an Azure AD administrator group named DBAs for the managed instance named ManagedInstance01.</span></span>
<span data-ttu-id="49e09-121">此伺服器與資源群組 ResourceGroup01 相關聯。</span><span class="sxs-lookup"><span data-stu-id="49e09-121">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="49e09-122">範例 2：使用受管理的實例物件來提供系統管理員使用者</span><span class="sxs-lookup"><span data-stu-id="49e09-122">Example 2: Provision an administrator user using managed instance object</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdministrator -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
Resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="49e09-123">此命令會從受管理的實例物件中將 Azure AD 使用者以系統管理員的名名提供。</span><span class="sxs-lookup"><span data-stu-id="49e09-123">This command provisions an Azure AD user as an administrator from the managed instance object.</span></span>

### <span data-ttu-id="49e09-124">範例 3：使用受管理的實例資源識別碼來提供系統管理員</span><span class="sxs-lookup"><span data-stu-id="49e09-124">Example 3: Provision an administrator using managed instance resource identifier</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdministrator -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
Resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="49e09-125">此命令會使用受管理的實例資源識別碼，將 Azure AD 使用者以系統管理員的名名提供。</span><span class="sxs-lookup"><span data-stu-id="49e09-125">This command provisions an Azure AD user as an administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="49e09-126">參數</span><span class="sxs-lookup"><span data-stu-id="49e09-126">PARAMETERS</span></span>

### <span data-ttu-id="49e09-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49e09-127">-DefaultProfile</span></span>
<span data-ttu-id="49e09-128">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="49e09-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49e09-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="49e09-129">-DisplayName</span></span>
<span data-ttu-id="49e09-130">指定要授予許可權的使用者或群組的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="49e09-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="49e09-131">此顯示名稱必須存在於與目前訂閱相關聯的 Active Directory 中。</span><span class="sxs-lookup"><span data-stu-id="49e09-131">This display name must exist in the active directory associated with the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49e09-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49e09-132">-InputObject</span></span>
<span data-ttu-id="49e09-133">這是要使用的受管理實例物件。</span><span class="sxs-lookup"><span data-stu-id="49e09-133">The managed instance object to use.</span></span>

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

### <span data-ttu-id="49e09-134">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="49e09-134">-InstanceName</span></span>
<span data-ttu-id="49e09-135">SQL Managed 實例名稱。</span><span class="sxs-lookup"><span data-stu-id="49e09-135">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="49e09-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="49e09-136">-ObjectId</span></span>
<span data-ttu-id="49e09-137">指定 Azure Active Directory 中使用者或群組的物件識別碼，以授予許可權。</span><span class="sxs-lookup"><span data-stu-id="49e09-137">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49e09-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49e09-138">-ResourceGroupName</span></span>
<span data-ttu-id="49e09-139">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="49e09-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="49e09-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49e09-140">-ResourceId</span></span>
<span data-ttu-id="49e09-141">要使用實例的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="49e09-141">The resource id of instance to use</span></span>

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

### <span data-ttu-id="49e09-142">-確認</span><span class="sxs-lookup"><span data-stu-id="49e09-142">-Confirm</span></span>
<span data-ttu-id="49e09-143">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="49e09-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49e09-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49e09-144">-WhatIf</span></span>
<span data-ttu-id="49e09-145">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="49e09-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49e09-146">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="49e09-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49e09-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49e09-147">CommonParameters</span></span>
<span data-ttu-id="49e09-148">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="49e09-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49e09-149">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49e09-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49e09-150">輸入</span><span class="sxs-lookup"><span data-stu-id="49e09-150">INPUTS</span></span>

### <span data-ttu-id="49e09-151">System.String</span><span class="sxs-lookup"><span data-stu-id="49e09-151">System.String</span></span>

### <span data-ttu-id="49e09-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="49e09-152">System.Guid</span></span>

## <span data-ttu-id="49e09-153">輸出</span><span class="sxs-lookup"><span data-stu-id="49e09-153">OUTPUTS</span></span>

### <span data-ttu-id="49e09-154">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="49e09-154">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="49e09-155">筆記</span><span class="sxs-lookup"><span data-stu-id="49e09-155">NOTES</span></span>

## <span data-ttu-id="49e09-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="49e09-156">RELATED LINKS</span></span>

[<span data-ttu-id="49e09-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="49e09-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="49e09-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="49e09-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
