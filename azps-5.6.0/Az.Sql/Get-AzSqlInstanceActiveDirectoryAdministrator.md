---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 0638e44f9f1c8febcbb9700fce1b9c4c9d5e410c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917562"
---
# <span data-ttu-id="140c1-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="140c1-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="140c1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="140c1-102">SYNOPSIS</span></span>
<span data-ttu-id="140c1-103">獲得 SQL Managed 實例的 Azure AD 系統管理員相關資訊。</span><span class="sxs-lookup"><span data-stu-id="140c1-103">Gets information about an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="140c1-104">語法</span><span class="sxs-lookup"><span data-stu-id="140c1-104">SYNTAX</span></span>

### <span data-ttu-id="140c1-105">UseResourceGroupAndInstanceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="140c1-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="140c1-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="140c1-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="140c1-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="140c1-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="140c1-108">描述</span><span class="sxs-lookup"><span data-stu-id="140c1-108">DESCRIPTION</span></span>
<span data-ttu-id="140c1-109">**Get-AzSqlInstanceActiveDirectoryAdministrator** Cmdlet 會取得目前訂閱中 Azure Active Directory (Azure AD) 系統管理員的 Azure Active Directory) 系統管理員相關資訊。</span><span class="sxs-lookup"><span data-stu-id="140c1-109">The **Get-AzSqlInstanceActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="140c1-110">例子</span><span class="sxs-lookup"><span data-stu-id="140c1-110">EXAMPLES</span></span>

### <span data-ttu-id="140c1-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="140c1-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="140c1-112">此命令會針對名為 ManagedInstance01 的受管理實例，獲得與名為 ResourceGroup01 的資源群組相關聯的 Azure AD 系統管理員相關資訊。</span><span class="sxs-lookup"><span data-stu-id="140c1-112">This command gets information about an Azure AD administrator for a managed instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="140c1-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="140c1-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="140c1-114">此命令會從受管理的實例物件中，獲得 Azure AD 系統管理員相關資訊。</span><span class="sxs-lookup"><span data-stu-id="140c1-114">This command gets information about an Azure AD administrator from a managed instance object.</span></span>

### <span data-ttu-id="140c1-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="140c1-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="140c1-116">此命令會使用受管理的實例資源識別碼，獲得有關 Azure AD 系統管理員的資訊。</span><span class="sxs-lookup"><span data-stu-id="140c1-116">This command gets information about an Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="140c1-117">參數</span><span class="sxs-lookup"><span data-stu-id="140c1-117">PARAMETERS</span></span>

### <span data-ttu-id="140c1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="140c1-118">-DefaultProfile</span></span>
<span data-ttu-id="140c1-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="140c1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="140c1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="140c1-120">-InputObject</span></span>
<span data-ttu-id="140c1-121">這是要使用的受管理實例物件。</span><span class="sxs-lookup"><span data-stu-id="140c1-121">The managed instance object to use.</span></span>

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

### <span data-ttu-id="140c1-122">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="140c1-122">-InstanceName</span></span>
<span data-ttu-id="140c1-123">SQL Managed 實例名稱。</span><span class="sxs-lookup"><span data-stu-id="140c1-123">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="140c1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="140c1-124">-ResourceGroupName</span></span>
<span data-ttu-id="140c1-125">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="140c1-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="140c1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="140c1-126">-ResourceId</span></span>
<span data-ttu-id="140c1-127">要使用實例的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="140c1-127">The resource id of instance to use</span></span>

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

### <span data-ttu-id="140c1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="140c1-128">CommonParameters</span></span>
<span data-ttu-id="140c1-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="140c1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="140c1-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="140c1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="140c1-131">輸入</span><span class="sxs-lookup"><span data-stu-id="140c1-131">INPUTS</span></span>

### <span data-ttu-id="140c1-132">System.String</span><span class="sxs-lookup"><span data-stu-id="140c1-132">System.String</span></span>

## <span data-ttu-id="140c1-133">輸出</span><span class="sxs-lookup"><span data-stu-id="140c1-133">OUTPUTS</span></span>

### <span data-ttu-id="140c1-134">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="140c1-134">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="140c1-135">筆記</span><span class="sxs-lookup"><span data-stu-id="140c1-135">NOTES</span></span>

## <span data-ttu-id="140c1-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="140c1-136">RELATED LINKS</span></span>

[<span data-ttu-id="140c1-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="140c1-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="140c1-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="140c1-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
