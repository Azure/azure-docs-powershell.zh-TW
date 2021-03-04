---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 8C5D29AD-0B15-4CD4-8637-86ABD19F41C8
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
ms.openlocfilehash: 7c45cb511fe1466aa2ac210ceeb2b609f6c0e97a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912557"
---
# <span data-ttu-id="7e18e-101">Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="7e18e-101">Get-AzSqlCapability</span></span>

## <span data-ttu-id="7e18e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7e18e-102">SYNOPSIS</span></span>
<span data-ttu-id="7e18e-103">為目前的訂閱獲得 SQL Database 功能。</span><span class="sxs-lookup"><span data-stu-id="7e18e-103">Gets SQL Database capabilities for the current subscription.</span></span>

## <span data-ttu-id="7e18e-104">語法</span><span class="sxs-lookup"><span data-stu-id="7e18e-104">SYNTAX</span></span>

### <span data-ttu-id="7e18e-105">FilterResults (預設) </span><span class="sxs-lookup"><span data-stu-id="7e18e-105">FilterResults (Default)</span></span>
```
Get-AzSqlCapability [-LocationName] <String> [-ServerVersionName <String>] [-EditionName <String>]
 [-ServiceObjectiveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e18e-106">DefaultResults</span><span class="sxs-lookup"><span data-stu-id="7e18e-106">DefaultResults</span></span>
```
Get-AzSqlCapability [-LocationName] <String> [-Defaults] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e18e-107">描述</span><span class="sxs-lookup"><span data-stu-id="7e18e-107">DESCRIPTION</span></span>
<span data-ttu-id="7e18e-108">**Get-AzSqlCapability** Cmdlet 會取得目前地區訂閱提供的 Azure SQL Database 功能。</span><span class="sxs-lookup"><span data-stu-id="7e18e-108">The **Get-AzSqlCapability** cmdlet gets the Azure SQL Database capabilities available on the current subscription for a region.</span></span>
<span data-ttu-id="7e18e-109">如果您指定 *ServerVersionName、EditionName* 或 *ServiceObjectiveName* 參數，此 Cmdlet 會返回指定的值及其前置專案。</span><span class="sxs-lookup"><span data-stu-id="7e18e-109">If you specify the *ServerVersionName*, *EditionName*, or *ServiceObjectiveName* parameters, this cmdlet returns the specified values and their predecessors.</span></span>

## <span data-ttu-id="7e18e-110">例子</span><span class="sxs-lookup"><span data-stu-id="7e18e-110">EXAMPLES</span></span>

### <span data-ttu-id="7e18e-111">範例 1：取得地區目前訂閱的功能</span><span class="sxs-lookup"><span data-stu-id="7e18e-111">Example 1: Get capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US"
Location                : Central US
Status                  : Available
SupportedServerVersions : {12.0, 2.0}
```

<span data-ttu-id="7e18e-112">此命令會針對美國中地區的目前訂閱，會針對 SQL Database 實例所執行的功能。</span><span class="sxs-lookup"><span data-stu-id="7e18e-112">This command returns the capabilities for SQL Database instances on the current subscription for the Central US region.</span></span>

### <span data-ttu-id="7e18e-113">範例 2：取得區域目前訂閱的預設功能</span><span class="sxs-lookup"><span data-stu-id="7e18e-113">Example 2: Get default capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -Defaults
Location        : Central US
Status          : Available
ExpandedDetails : Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S0 (Default)
```

<span data-ttu-id="7e18e-114">此命令會針對美國中區目前訂閱的 SQL 資料庫，會返回預設功能。</span><span class="sxs-lookup"><span data-stu-id="7e18e-114">This command returns the default capabilities for SQL Databases on the current subscription in the Central US region.</span></span>

### <span data-ttu-id="7e18e-115">範例 3：取得服務目標的詳細資訊</span><span class="sxs-lookup"><span data-stu-id="7e18e-115">Example 3: Get details for a service objective</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -ServiceObjectiveName "S1"
Location        : Central US
Status          : Available
ExpandedDetails : Version: 12.0 (Available) -> Edition: Standard (Default) -> Service Objective: S1 (Available) 
                  Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S1 (Available)
```

<span data-ttu-id="7e18e-116">此命令會針對目前訂閱上指定的服務目標，獲得 SQL 資料庫的預設功能。</span><span class="sxs-lookup"><span data-stu-id="7e18e-116">This command gets default capabilities for SQL Databases for the specified service objective on the current subscription.</span></span>

## <span data-ttu-id="7e18e-117">參數</span><span class="sxs-lookup"><span data-stu-id="7e18e-117">PARAMETERS</span></span>

### <span data-ttu-id="7e18e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e18e-118">-DefaultProfile</span></span>
<span data-ttu-id="7e18e-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="7e18e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e18e-120">-預設值</span><span class="sxs-lookup"><span data-stu-id="7e18e-120">-Defaults</span></span>
<span data-ttu-id="7e18e-121">表示此 Cmdlet 僅會獲得預設值。</span><span class="sxs-lookup"><span data-stu-id="7e18e-121">Indicates that this cmdlet gets only defaults.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e18e-122">-EditionName</span><span class="sxs-lookup"><span data-stu-id="7e18e-122">-EditionName</span></span>
<span data-ttu-id="7e18e-123">指定此 Cmdlet 可獲取功能的資料庫版本名稱。</span><span class="sxs-lookup"><span data-stu-id="7e18e-123">Specifies the name of the database edition for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e18e-124">-LocationName</span><span class="sxs-lookup"><span data-stu-id="7e18e-124">-LocationName</span></span>
<span data-ttu-id="7e18e-125">指定此 Cmdlet 可獲取功能的位置名稱。</span><span class="sxs-lookup"><span data-stu-id="7e18e-125">Specifies the name of the Location for which this cmdlet gets capabilities.</span></span>
<span data-ttu-id="7e18e-126">詳細資訊請參閱 Azure 區域 http://azure.microsoft.com/en-us/regions/ http://azure.microsoft.com/en-us/regions/) (。</span><span class="sxs-lookup"><span data-stu-id="7e18e-126">For more information, see Azure Regionshttp://azure.microsoft.com/en-us/regions/ (http://azure.microsoft.com/en-us/regions/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e18e-127">-ServerVersionName</span><span class="sxs-lookup"><span data-stu-id="7e18e-127">-ServerVersionName</span></span>
<span data-ttu-id="7e18e-128">指定此 Cmdlet 可獲取功能的伺服器版本名稱。</span><span class="sxs-lookup"><span data-stu-id="7e18e-128">Specifies the name of the server version for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e18e-129">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="7e18e-129">-ServiceObjectiveName</span></span>
<span data-ttu-id="7e18e-130">指定此 Cmdlet 可獲取功能的服務目標名稱。</span><span class="sxs-lookup"><span data-stu-id="7e18e-130">Specifies the name of the service objective for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e18e-131">-確認</span><span class="sxs-lookup"><span data-stu-id="7e18e-131">-Confirm</span></span>
<span data-ttu-id="7e18e-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7e18e-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e18e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e18e-133">-WhatIf</span></span>
<span data-ttu-id="7e18e-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7e18e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e18e-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7e18e-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e18e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e18e-136">CommonParameters</span></span>
<span data-ttu-id="7e18e-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7e18e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e18e-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e18e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e18e-139">輸入</span><span class="sxs-lookup"><span data-stu-id="7e18e-139">INPUTS</span></span>

### <span data-ttu-id="7e18e-140">System.String</span><span class="sxs-lookup"><span data-stu-id="7e18e-140">System.String</span></span>

## <span data-ttu-id="7e18e-141">輸出</span><span class="sxs-lookup"><span data-stu-id="7e18e-141">OUTPUTS</span></span>

### <span data-ttu-id="7e18e-142">Microsoft.Azure.Commands.Sql.Location_Capabilities.Model.LocationCapabilityModel</span><span class="sxs-lookup"><span data-stu-id="7e18e-142">Microsoft.Azure.Commands.Sql.Location_Capabilities.Model.LocationCapabilityModel</span></span>

## <span data-ttu-id="7e18e-143">筆記</span><span class="sxs-lookup"><span data-stu-id="7e18e-143">NOTES</span></span>

## <span data-ttu-id="7e18e-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="7e18e-144">RELATED LINKS</span></span>
