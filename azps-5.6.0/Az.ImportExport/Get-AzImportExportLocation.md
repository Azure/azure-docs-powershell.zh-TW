---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/get-azimportexportlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
ms.openlocfilehash: 928ac0254619a2924421a0b52bf20212b8ba19a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904669"
---
# <span data-ttu-id="0e447-101">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="0e447-101">Get-AzImportExportLocation</span></span>

## <span data-ttu-id="0e447-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0e447-102">SYNOPSIS</span></span>
<span data-ttu-id="0e447-103">會返回可以出貨與匯進或匯出工作相關之磁片的位置詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0e447-103">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="0e447-104">位置是 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="0e447-104">A location is an Azure region.</span></span>

## <span data-ttu-id="0e447-105">語法</span><span class="sxs-lookup"><span data-stu-id="0e447-105">SYNTAX</span></span>

### <span data-ttu-id="0e447-106">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="0e447-106">List (Default)</span></span>
```
Get-AzImportExportLocation [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0e447-107">獲取</span><span class="sxs-lookup"><span data-stu-id="0e447-107">Get</span></span>
```
Get-AzImportExportLocation -Name <String> [-AcceptLanguage <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e447-108">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0e447-108">GetViaIdentity</span></span>
```
Get-AzImportExportLocation -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0e447-109">描述</span><span class="sxs-lookup"><span data-stu-id="0e447-109">DESCRIPTION</span></span>
<span data-ttu-id="0e447-110">會返回可以出貨與匯進或匯出工作相關之磁片的位置詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0e447-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="0e447-111">位置是 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="0e447-111">A location is an Azure region.</span></span>

## <span data-ttu-id="0e447-112">例子</span><span class="sxs-lookup"><span data-stu-id="0e447-112">EXAMPLES</span></span>

### <span data-ttu-id="0e447-113">範例 1：使用預設上下文取得所有 Azure 地區位置詳細資料</span><span class="sxs-lookup"><span data-stu-id="0e447-113">Example 1: Get all Azure region location details with default context</span></span>
```powershell
PS C:\> Get-AzImportExportLocation
Name                 Type
----                 ----
Australia East       Microsoft.ImportExport/locations
Australia Southeast  Microsoft.ImportExport/locations
Brazil South         Microsoft.ImportExport/locations
Canada Central       Microsoft.ImportExport/locations
Canada East          Microsoft.ImportExport/locations
...
West Central US      Microsoft.ImportExport/locations
West Europe          Microsoft.ImportExport/locations
West India           Microsoft.ImportExport/locations
West US              Microsoft.ImportExport/locations
West US 2            Microsoft.ImportExport/locations
```

<span data-ttu-id="0e447-114">此 Cmdlet 會以預設上下文獲得所有 Azure 地區位置詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0e447-114">This cmdlet gets all Azure region location details with default context.</span></span>

### <span data-ttu-id="0e447-115">範例 2：根據位置名稱取得 Azure 地區位置詳細資料</span><span class="sxs-lookup"><span data-stu-id="0e447-115">Example 2: Get Azure region location details by location name</span></span>
```powershell
PS C:\> Get-AzImportExportLocation -Name eastus
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="0e447-116">此 Cmdlet 會根據位置名稱，獲得 Azure 地區位置詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0e447-116">This cmdlet gets Azure region location details by location name.</span></span>

### <span data-ttu-id="0e447-117">範例 3：根據身分識別取得 Azure 地區位置詳細資料</span><span class="sxs-lookup"><span data-stu-id="0e447-117">Example 3: Get Azure region location details by identity</span></span>
```powershell
PS C:\> $Id = "/providers/Microsoft.ImportExport/locations/eastus"
PS C:\> Get-AzImportExportLocation -InputObject $Id
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="0e447-118">此 Cmdlet 清單會以身分識別獲得 Azure 地區位置詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0e447-118">This cmdlet lists gets Azure region location details by identity.</span></span>

## <span data-ttu-id="0e447-119">參數</span><span class="sxs-lookup"><span data-stu-id="0e447-119">PARAMETERS</span></span>

### <span data-ttu-id="0e447-120">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="0e447-120">-AcceptLanguage</span></span>
<span data-ttu-id="0e447-121">指定回應的偏好語言。</span><span class="sxs-lookup"><span data-stu-id="0e447-121">Specifies the preferred language for the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e447-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e447-122">-DefaultProfile</span></span>
<span data-ttu-id="0e447-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0e447-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e447-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e447-124">-InputObject</span></span>
<span data-ttu-id="0e447-125">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="0e447-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e447-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="0e447-126">-Name</span></span>
<span data-ttu-id="0e447-127">位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e447-127">The name of the location.</span></span>
<span data-ttu-id="0e447-128">例如，美國西部或西部。</span><span class="sxs-lookup"><span data-stu-id="0e447-128">For example, West US or westus.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: LocationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e447-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e447-129">CommonParameters</span></span>
<span data-ttu-id="0e447-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0e447-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e447-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e447-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e447-132">輸入</span><span class="sxs-lookup"><span data-stu-id="0e447-132">INPUTS</span></span>

### <span data-ttu-id="0e447-133">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="0e447-133">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="0e447-134">輸出</span><span class="sxs-lookup"><span data-stu-id="0e447-134">OUTPUTS</span></span>

### <span data-ttu-id="0e447-135">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.models.Api20161101.ILocation</span><span class="sxs-lookup"><span data-stu-id="0e447-135">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation</span></span>

## <span data-ttu-id="0e447-136">筆記</span><span class="sxs-lookup"><span data-stu-id="0e447-136">NOTES</span></span>

<span data-ttu-id="0e447-137">別名</span><span class="sxs-lookup"><span data-stu-id="0e447-137">ALIASES</span></span>

<span data-ttu-id="0e447-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="0e447-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0e447-139">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="0e447-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0e447-140">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="0e447-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0e447-141">INPUTOBJECT： <IImportExportIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="0e447-141">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0e447-142">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="0e447-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0e447-143">`[JobName <String>]`：匯進/匯出工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e447-143">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="0e447-144">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e447-144">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="0e447-145">例如，美國西部或西部。</span><span class="sxs-lookup"><span data-stu-id="0e447-145">For example, West US or westus.</span></span>
  - <span data-ttu-id="0e447-146">`[ResourceGroupName <String>]`：資源組名可唯一識別使用者訂閱中的資源群組。</span><span class="sxs-lookup"><span data-stu-id="0e447-146">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="0e447-147">`[SubscriptionId <String>]`：Azure 使用者的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="0e447-147">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="0e447-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="0e447-148">RELATED LINKS</span></span>

