---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 8C5D29AD-0B15-4CD4-8637-86ABD19F41C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
ms.openlocfilehash: 582b512ef502e0dac3fc443807f1e33a65063728
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129212"
---
# <span data-ttu-id="4c892-101">Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="4c892-101">Get-AzSqlCapability</span></span>

## <span data-ttu-id="4c892-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4c892-102">SYNOPSIS</span></span>
<span data-ttu-id="4c892-103">取得目前訂閱的 SQL 資料庫功能。</span><span class="sxs-lookup"><span data-stu-id="4c892-103">Gets SQL Database capabilities for the current subscription.</span></span>

## <span data-ttu-id="4c892-104">句法</span><span class="sxs-lookup"><span data-stu-id="4c892-104">SYNTAX</span></span>

### <span data-ttu-id="4c892-105">FilterResults (預設) </span><span class="sxs-lookup"><span data-stu-id="4c892-105">FilterResults (Default)</span></span>
```
Get-AzSqlCapability [-LocationName] <String> [-ServerVersionName <String>] [-EditionName <String>]
 [-ServiceObjectiveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4c892-106">DefaultResults</span><span class="sxs-lookup"><span data-stu-id="4c892-106">DefaultResults</span></span>
```
Get-AzSqlCapability [-LocationName] <String> [-Defaults] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c892-107">說明</span><span class="sxs-lookup"><span data-stu-id="4c892-107">DESCRIPTION</span></span>
<span data-ttu-id="4c892-108">**AzSqlCapability** Cmdlet 會取得在目前的區域訂閱中提供的 Azure SQL 資料庫功能。</span><span class="sxs-lookup"><span data-stu-id="4c892-108">The **Get-AzSqlCapability** cmdlet gets the Azure SQL Database capabilities available on the current subscription for a region.</span></span>
<span data-ttu-id="4c892-109">如果您指定 *ServerVersionName* 、 *EditionName* 或 *ServiceObjectiveName* 參數，這個 Cmdlet 會傳回指定的值及其前置任務。</span><span class="sxs-lookup"><span data-stu-id="4c892-109">If you specify the *ServerVersionName* , *EditionName* , or *ServiceObjectiveName* parameters, this cmdlet returns the specified values and their predecessors.</span></span>

## <span data-ttu-id="4c892-110">示例</span><span class="sxs-lookup"><span data-stu-id="4c892-110">EXAMPLES</span></span>

### <span data-ttu-id="4c892-111">範例1：取得某個地區目前訂閱的功能</span><span class="sxs-lookup"><span data-stu-id="4c892-111">Example 1: Get capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US"
Location                : Central US
Status                  : Available
SupportedServerVersions : {12.0, 2.0}
```

<span data-ttu-id="4c892-112">這個命令會傳回目前訂閱中美國中部地區的 SQL 資料庫實例的功能。</span><span class="sxs-lookup"><span data-stu-id="4c892-112">This command returns the capabilities for SQL Database instances on the current subscription for the Central US region.</span></span>

### <span data-ttu-id="4c892-113">範例2：取得某個地區目前訂閱的預設功能</span><span class="sxs-lookup"><span data-stu-id="4c892-113">Example 2: Get default capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -Defaults
Location        : Central US
Status          : Available
ExpandedDetails : Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S0 (Default)
```

<span data-ttu-id="4c892-114">這個命令會傳回目前訂閱中的 SQL 資料庫的預設功能（位於美國中北部區域）。</span><span class="sxs-lookup"><span data-stu-id="4c892-114">This command returns the default capabilities for SQL Databases on the current subscription in the Central US region.</span></span>

### <span data-ttu-id="4c892-115">範例3：取得服務目標的詳細資料</span><span class="sxs-lookup"><span data-stu-id="4c892-115">Example 3: Get details for a service objective</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -ServiceObjectiveName "S1"
Location        : Central US
Status          : Available
ExpandedDetails : Version: 12.0 (Available) -> Edition: Standard (Default) -> Service Objective: S1 (Available) 
                  Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S1 (Available)
```

<span data-ttu-id="4c892-116">這個命令會針對目前訂閱上的指定服務目標，取得 SQL 資料庫的預設功能。</span><span class="sxs-lookup"><span data-stu-id="4c892-116">This command gets default capabilities for SQL Databases for the specified service objective on the current subscription.</span></span>

## <span data-ttu-id="4c892-117">參數</span><span class="sxs-lookup"><span data-stu-id="4c892-117">PARAMETERS</span></span>

### <span data-ttu-id="4c892-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c892-118">-DefaultProfile</span></span>
<span data-ttu-id="4c892-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4c892-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c892-120">-預設值</span><span class="sxs-lookup"><span data-stu-id="4c892-120">-Defaults</span></span>
<span data-ttu-id="4c892-121">表示此 Cmdlet 只會取得預設值。</span><span class="sxs-lookup"><span data-stu-id="4c892-121">Indicates that this cmdlet gets only defaults.</span></span>

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

### <span data-ttu-id="4c892-122">-EditionName</span><span class="sxs-lookup"><span data-stu-id="4c892-122">-EditionName</span></span>
<span data-ttu-id="4c892-123">指定此 Cmdlet 取得功能之資料庫版本的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c892-123">Specifies the name of the database edition for which this cmdlet gets capabilities.</span></span>

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

### <span data-ttu-id="4c892-124">-LocationName</span><span class="sxs-lookup"><span data-stu-id="4c892-124">-LocationName</span></span>
<span data-ttu-id="4c892-125">指定此 Cmdlet 取得功能的位置名稱。</span><span class="sxs-lookup"><span data-stu-id="4c892-125">Specifies the name of the Location for which this cmdlet gets capabilities.</span></span>
<span data-ttu-id="4c892-126">如需詳細資訊，請參閱 Azure 地區 http://azure.microsoft.com/en-us/regions/ (http://azure.microsoft.com/en-us/regions/) 。</span><span class="sxs-lookup"><span data-stu-id="4c892-126">For more information, see Azure Regionshttp://azure.microsoft.com/en-us/regions/ (http://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="4c892-127">-ServerVersionName</span><span class="sxs-lookup"><span data-stu-id="4c892-127">-ServerVersionName</span></span>
<span data-ttu-id="4c892-128">指定此 Cmdlet 取得功能之伺服器版本的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c892-128">Specifies the name of the server version for which this cmdlet gets capabilities.</span></span>

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

### <span data-ttu-id="4c892-129">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="4c892-129">-ServiceObjectiveName</span></span>
<span data-ttu-id="4c892-130">指定此 Cmdlet 取得功能之服務目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c892-130">Specifies the name of the service objective for which this cmdlet gets capabilities.</span></span>

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

### <span data-ttu-id="4c892-131">-確認</span><span class="sxs-lookup"><span data-stu-id="4c892-131">-Confirm</span></span>
<span data-ttu-id="4c892-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4c892-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c892-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c892-133">-WhatIf</span></span>
<span data-ttu-id="4c892-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4c892-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c892-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4c892-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c892-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c892-136">CommonParameters</span></span>
<span data-ttu-id="4c892-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4c892-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c892-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4c892-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c892-139">輸入</span><span class="sxs-lookup"><span data-stu-id="4c892-139">INPUTS</span></span>

### <span data-ttu-id="4c892-140">System.object</span><span class="sxs-lookup"><span data-stu-id="4c892-140">System.String</span></span>

## <span data-ttu-id="4c892-141">輸出</span><span class="sxs-lookup"><span data-stu-id="4c892-141">OUTPUTS</span></span>

### <span data-ttu-id="4c892-142">Microsoft.Azure.Commands.Sql.Location_Capabilities LocationCapabilityModel</span><span class="sxs-lookup"><span data-stu-id="4c892-142">Microsoft.Azure.Commands.Sql.Location_Capabilities.Model.LocationCapabilityModel</span></span>

## <span data-ttu-id="4c892-143">筆記</span><span class="sxs-lookup"><span data-stu-id="4c892-143">NOTES</span></span>

## <span data-ttu-id="4c892-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="4c892-144">RELATED LINKS</span></span>