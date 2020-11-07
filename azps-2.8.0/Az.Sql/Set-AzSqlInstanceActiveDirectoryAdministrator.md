---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 8a034bc85209e0325547bac2f64f277ceaee0abc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792640"
---
# <span data-ttu-id="c0cfd-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="c0cfd-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="c0cfd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c0cfd-102">SYNOPSIS</span></span>
<span data-ttu-id="c0cfd-103">為 SQL 管理實例提供 Azure AD 系統管理員。</span><span class="sxs-lookup"><span data-stu-id="c0cfd-103">Provisions an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="c0cfd-104">句法</span><span class="sxs-lookup"><span data-stu-id="c0cfd-104">SYNTAX</span></span>

### <span data-ttu-id="c0cfd-105">UseResourceGroupAndInstanceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c0cfd-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0cfd-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0cfd-106">UseInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 [-InputObject <AzureSqlManagedInstanceModel>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0cfd-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0cfd-107">UserResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0cfd-108">說明</span><span class="sxs-lookup"><span data-stu-id="c0cfd-108">DESCRIPTION</span></span>
<span data-ttu-id="c0cfd-109">**AzSqlInstanceActiveDirectoryAdministrator** Cmdlet 會將 Azure Active Directory (azure AD) 管理員提供給目前訂閱中的 AzureSQL Managed 實例。</span><span class="sxs-lookup"><span data-stu-id="c0cfd-109">The **Set-AzSqlInstanceActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>
<span data-ttu-id="c0cfd-110">您一次只能提供一個系統管理員。</span><span class="sxs-lookup"><span data-stu-id="c0cfd-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="c0cfd-111">下列 Azure AD 的成員可設為 SQL Managed 實例系統管理員：</span><span class="sxs-lookup"><span data-stu-id="c0cfd-111">The following members of Azure AD can be provisioned as a SQL Managed Instance administrator:</span></span>
- <span data-ttu-id="c0cfd-112">Azure AD 的原生成員</span><span class="sxs-lookup"><span data-stu-id="c0cfd-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="c0cfd-113">Azure AD 的聯合成員</span><span class="sxs-lookup"><span data-stu-id="c0cfd-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="c0cfd-114">作為安全性群組而建立的 Azure AD 群組不支援從其他 Azure ADs 匯入成員。</span><span class="sxs-lookup"><span data-stu-id="c0cfd-114">Azure AD groups created as security groups Imported members from other Azure ADs are not supported as administrators.</span></span>
<span data-ttu-id="c0cfd-115">Microsoft 帳戶（例如 Outlook.com、Hotmail.com 或 Live.com 網域中的帳戶）不受系統管理員支援。</span><span class="sxs-lookup"><span data-stu-id="c0cfd-115">Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="c0cfd-116">其他來賓帳戶（例如 Gmail.com 或 Yahoo.com 網域中的帳戶）不受系統管理員支援。</span><span class="sxs-lookup"><span data-stu-id="c0cfd-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="c0cfd-117">我們建議您以系統管理員身分提供專用的 Azure AD 群組。</span><span class="sxs-lookup"><span data-stu-id="c0cfd-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="c0cfd-118">示例</span><span class="sxs-lookup"><span data-stu-id="c0cfd-118">EXAMPLES</span></span>

### <span data-ttu-id="c0cfd-119">範例1：為與資源群組相關聯的受管理實例提供管理員群組</span><span class="sxs-lookup"><span data-stu-id="c0cfd-119">Example 1: Provision an administrator group for a managed instance associated with resource group</span></span>
```
PS C:\>Set-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="c0cfd-120">這個命令會為名為 ManagedInstance01 的 managed 實例提供名為 Dba 的 Azure AD 管理員群組。</span><span class="sxs-lookup"><span data-stu-id="c0cfd-120">This command provisions an Azure AD administrator group named DBAs for the managed instance named ManagedInstance01.</span></span>
<span data-ttu-id="c0cfd-121">此伺服器與資源群組 ResourceGroup01 相關聯。</span><span class="sxs-lookup"><span data-stu-id="c0cfd-121">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="c0cfd-122">範例2：使用 managed 實例物件提供管理員使用者</span><span class="sxs-lookup"><span data-stu-id="c0cfd-122">Example 2: Provision an administrator user using managed instance object</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdmin -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="c0cfd-123">這個命令會以系統管理員身分為 managed 實例物件來置備 Azure AD 使用者。</span><span class="sxs-lookup"><span data-stu-id="c0cfd-123">This command provisions an Azure AD user as an administrator from the managed instance object.</span></span>

### <span data-ttu-id="c0cfd-124">範例3：使用 managed 實例資源識別碼來提供管理員</span><span class="sxs-lookup"><span data-stu-id="c0cfd-124">Example 3: Provision an administrator using managed instance resource identifier</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdmin -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="c0cfd-125">這個命令會以系統管理員身分使用 managed 實例資源識別碼來置備 Azure AD 使用者。</span><span class="sxs-lookup"><span data-stu-id="c0cfd-125">This command provisions an Azure AD user as an administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="c0cfd-126">參數</span><span class="sxs-lookup"><span data-stu-id="c0cfd-126">PARAMETERS</span></span>

### <span data-ttu-id="c0cfd-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0cfd-127">-DefaultProfile</span></span>
<span data-ttu-id="c0cfd-128">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0cfd-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0cfd-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c0cfd-129">-DisplayName</span></span>
<span data-ttu-id="c0cfd-130">指定要授與許可權的使用者或群組的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c0cfd-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="c0cfd-131">此顯示名稱必須存在於與目前訂閱相關聯的 active directory 中。</span><span class="sxs-lookup"><span data-stu-id="c0cfd-131">This display name must exist in the active directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="c0cfd-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0cfd-132">-InputObject</span></span>
<span data-ttu-id="c0cfd-133">要使用的 managed 實例物件。</span><span class="sxs-lookup"><span data-stu-id="c0cfd-133">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0cfd-134">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c0cfd-134">-InstanceName</span></span>
<span data-ttu-id="c0cfd-135">SQL Managed 實例名稱。</span><span class="sxs-lookup"><span data-stu-id="c0cfd-135">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="c0cfd-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c0cfd-136">-ObjectId</span></span>
<span data-ttu-id="c0cfd-137">指定 Azure Active Directory 中要授與許可權的使用者或群組物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="c0cfd-137">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

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

### <span data-ttu-id="c0cfd-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0cfd-138">-ResourceGroupName</span></span>
<span data-ttu-id="c0cfd-139">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0cfd-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="c0cfd-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0cfd-140">-ResourceId</span></span>
<span data-ttu-id="c0cfd-141">要使用之實例的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c0cfd-141">The resource id of instance to use</span></span>

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

### <span data-ttu-id="c0cfd-142">-確認</span><span class="sxs-lookup"><span data-stu-id="c0cfd-142">-Confirm</span></span>
<span data-ttu-id="c0cfd-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c0cfd-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0cfd-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0cfd-144">-WhatIf</span></span>
<span data-ttu-id="c0cfd-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c0cfd-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0cfd-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0cfd-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0cfd-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0cfd-147">CommonParameters</span></span>
<span data-ttu-id="c0cfd-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c0cfd-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0cfd-149">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c0cfd-149">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0cfd-150">輸入</span><span class="sxs-lookup"><span data-stu-id="c0cfd-150">INPUTS</span></span>

### <span data-ttu-id="c0cfd-151">System.object</span><span class="sxs-lookup"><span data-stu-id="c0cfd-151">System.String</span></span>

### <span data-ttu-id="c0cfd-152">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="c0cfd-152">System.Guid</span></span>

## <span data-ttu-id="c0cfd-153">輸出</span><span class="sxs-lookup"><span data-stu-id="c0cfd-153">OUTPUTS</span></span>

### <span data-ttu-id="c0cfd-154">AzureSqlInstanceActiveDirectoryAdministratorModel 中的 [InstanceActiveDirectoryAdministrator]</span><span class="sxs-lookup"><span data-stu-id="c0cfd-154">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="c0cfd-155">筆記</span><span class="sxs-lookup"><span data-stu-id="c0cfd-155">NOTES</span></span>

## <span data-ttu-id="c0cfd-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0cfd-156">RELATED LINKS</span></span>

[<span data-ttu-id="c0cfd-157">AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="c0cfd-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="c0cfd-158">移除-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="c0cfd-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
