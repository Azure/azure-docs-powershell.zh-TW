---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 90dade6f8ae40d007e7f5dc575c954b1d4ad639f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970125"
---
# <span data-ttu-id="7b8e2-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="7b8e2-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="7b8e2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7b8e2-102">SYNOPSIS</span></span>
<span data-ttu-id="7b8e2-103">取得適用于 SQL 管理實例的 Azure AD 管理員的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7b8e2-103">Gets information about an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="7b8e2-104">句法</span><span class="sxs-lookup"><span data-stu-id="7b8e2-104">SYNTAX</span></span>

### <span data-ttu-id="7b8e2-105">UseResourceGroupAndInstanceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7b8e2-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b8e2-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b8e2-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b8e2-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b8e2-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b8e2-108">說明</span><span class="sxs-lookup"><span data-stu-id="7b8e2-108">DESCRIPTION</span></span>
<span data-ttu-id="7b8e2-109">**AzSqlInstanceActiveDirectoryAdministrator** Cmdlet 會取得 Azure Active Directory 的相關資訊， (azure AD) 管理員取得目前訂閱中的 AzureSQL Managed 實例。</span><span class="sxs-lookup"><span data-stu-id="7b8e2-109">The **Get-AzSqlInstanceActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="7b8e2-110">示例</span><span class="sxs-lookup"><span data-stu-id="7b8e2-110">EXAMPLES</span></span>

### <span data-ttu-id="7b8e2-111">範例1</span><span class="sxs-lookup"><span data-stu-id="7b8e2-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="7b8e2-112">這個命令會取得與名為 ResourceGroup01 之資源群組相關聯之受管理實例的 Azure AD 系統管理員資訊。</span><span class="sxs-lookup"><span data-stu-id="7b8e2-112">This command gets information about an Azure AD administrator for a managed instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="7b8e2-113">範例2</span><span class="sxs-lookup"><span data-stu-id="7b8e2-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="7b8e2-114">這個命令會從受管理的實例物件取得 Azure AD 系統管理員的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7b8e2-114">This command gets information about an Azure AD administrator from a managed instance object.</span></span>

### <span data-ttu-id="7b8e2-115">範例3</span><span class="sxs-lookup"><span data-stu-id="7b8e2-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="7b8e2-116">這個命令會透過 managed 實例資源識別碼來取得 Azure AD 系統管理員的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7b8e2-116">This command gets information about an Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="7b8e2-117">參數</span><span class="sxs-lookup"><span data-stu-id="7b8e2-117">PARAMETERS</span></span>

### <span data-ttu-id="7b8e2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b8e2-118">-DefaultProfile</span></span>
<span data-ttu-id="7b8e2-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7b8e2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b8e2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b8e2-120">-InputObject</span></span>
<span data-ttu-id="7b8e2-121">要使用的 managed 實例物件。</span><span class="sxs-lookup"><span data-stu-id="7b8e2-121">The managed instance object to use.</span></span>

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

### <span data-ttu-id="7b8e2-122">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="7b8e2-122">-InstanceName</span></span>
<span data-ttu-id="7b8e2-123">SQL Managed 實例名稱。</span><span class="sxs-lookup"><span data-stu-id="7b8e2-123">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="7b8e2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b8e2-124">-ResourceGroupName</span></span>
<span data-ttu-id="7b8e2-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7b8e2-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="7b8e2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b8e2-126">-ResourceId</span></span>
<span data-ttu-id="7b8e2-127">要使用之實例的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="7b8e2-127">The resource id of instance to use</span></span>

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

### <span data-ttu-id="7b8e2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b8e2-128">CommonParameters</span></span>
<span data-ttu-id="7b8e2-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7b8e2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b8e2-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7b8e2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b8e2-131">輸入</span><span class="sxs-lookup"><span data-stu-id="7b8e2-131">INPUTS</span></span>

### <span data-ttu-id="7b8e2-132">System.object</span><span class="sxs-lookup"><span data-stu-id="7b8e2-132">System.String</span></span>

## <span data-ttu-id="7b8e2-133">輸出</span><span class="sxs-lookup"><span data-stu-id="7b8e2-133">OUTPUTS</span></span>

### <span data-ttu-id="7b8e2-134">AzureSqlInstanceActiveDirectoryAdministratorModel 中的 [InstanceActiveDirectoryAdministrator]</span><span class="sxs-lookup"><span data-stu-id="7b8e2-134">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="7b8e2-135">筆記</span><span class="sxs-lookup"><span data-stu-id="7b8e2-135">NOTES</span></span>

## <span data-ttu-id="7b8e2-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="7b8e2-136">RELATED LINKS</span></span>

[<span data-ttu-id="7b8e2-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="7b8e2-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="7b8e2-138">移除-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="7b8e2-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)