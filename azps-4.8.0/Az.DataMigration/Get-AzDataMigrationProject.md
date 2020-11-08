---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
ms.openlocfilehash: 7fe1e12c7c7feb2a47ac33b309b188e53e77fc73
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128239"
---
# <span data-ttu-id="380b0-101">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="380b0-101">Get-AzDataMigrationProject</span></span>

## <span data-ttu-id="380b0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="380b0-102">SYNOPSIS</span></span>
<span data-ttu-id="380b0-103">檢索 Azure 資料庫移轉專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="380b0-103">Retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="380b0-104">句法</span><span class="sxs-lookup"><span data-stu-id="380b0-104">SYNTAX</span></span>

### <span data-ttu-id="380b0-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="380b0-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="380b0-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="380b0-106">ComponentObjectParameterSet</span></span>
```
Get-AzDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="380b0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="380b0-107">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationProject [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="380b0-108">說明</span><span class="sxs-lookup"><span data-stu-id="380b0-108">DESCRIPTION</span></span>
<span data-ttu-id="380b0-109">Get-AzDataMigrationProject Cmdlet 會檢索 Azure 資料庫移轉專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="380b0-109">The Get-AzDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="380b0-110">示例</span><span class="sxs-lookup"><span data-stu-id="380b0-110">EXAMPLES</span></span>

### <span data-ttu-id="380b0-111">範例1</span><span class="sxs-lookup"><span data-stu-id="380b0-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="380b0-112">上述範例會在名為「testResourceGroup」的資源群組中檢索名為 TestProject 的 Azure 資料庫移轉專案，並在 [服務稱為 testService]</span><span class="sxs-lookup"><span data-stu-id="380b0-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="380b0-113">範例2</span><span class="sxs-lookup"><span data-stu-id="380b0-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationProject -InputObject $myService
```

<span data-ttu-id="380b0-114">上述範例會根據傳入的 PSProject 物件輸入參數，來檢索 Azure Database 移植專案。</span><span class="sxs-lookup"><span data-stu-id="380b0-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="380b0-115">參數</span><span class="sxs-lookup"><span data-stu-id="380b0-115">PARAMETERS</span></span>

### <span data-ttu-id="380b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="380b0-116">-DefaultProfile</span></span>
<span data-ttu-id="380b0-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="380b0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="380b0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="380b0-118">-InputObject</span></span>
<span data-ttu-id="380b0-119">PSDataMigrationService 物件。</span><span class="sxs-lookup"><span data-stu-id="380b0-119">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="380b0-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="380b0-120">-Name</span></span>
<span data-ttu-id="380b0-121">專案名稱。</span><span class="sxs-lookup"><span data-stu-id="380b0-121">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProjectName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380b0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="380b0-122">-ResourceGroupName</span></span>
<span data-ttu-id="380b0-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="380b0-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380b0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="380b0-124">-ResourceId</span></span>
<span data-ttu-id="380b0-125">DataMigrationService 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="380b0-125">DataMigrationService Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="380b0-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="380b0-126">-ServiceName</span></span>
<span data-ttu-id="380b0-127">資料庫移轉服務名稱。</span><span class="sxs-lookup"><span data-stu-id="380b0-127">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380b0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="380b0-128">CommonParameters</span></span>
<span data-ttu-id="380b0-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="380b0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="380b0-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="380b0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="380b0-131">輸入</span><span class="sxs-lookup"><span data-stu-id="380b0-131">INPUTS</span></span>

### <span data-ttu-id="380b0-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="380b0-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="380b0-133">System.object</span><span class="sxs-lookup"><span data-stu-id="380b0-133">System.String</span></span>

## <span data-ttu-id="380b0-134">輸出</span><span class="sxs-lookup"><span data-stu-id="380b0-134">OUTPUTS</span></span>

### <span data-ttu-id="380b0-135">PSProject 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="380b0-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="380b0-136">筆記</span><span class="sxs-lookup"><span data-stu-id="380b0-136">NOTES</span></span>

## <span data-ttu-id="380b0-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="380b0-137">RELATED LINKS</span></span>
