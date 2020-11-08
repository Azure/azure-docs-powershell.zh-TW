---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
ms.openlocfilehash: c603c01619128d1697256174e9d0bc00a1cea8ff
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128691"
---
# <span data-ttu-id="3bb98-101">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="3bb98-101">Get-AzImportExportLocation</span></span>

## <span data-ttu-id="3bb98-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3bb98-102">SYNOPSIS</span></span>
<span data-ttu-id="3bb98-103">傳回與匯入或匯出作業相關聯之磁片之位置的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3bb98-103">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="3bb98-104">位置是 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="3bb98-104">A location is an Azure region.</span></span>

## <span data-ttu-id="3bb98-105">句法</span><span class="sxs-lookup"><span data-stu-id="3bb98-105">SYNTAX</span></span>

### <span data-ttu-id="3bb98-106"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="3bb98-106">List (Default)</span></span>
```
Get-AzImportExportLocation [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3bb98-107">獲取</span><span class="sxs-lookup"><span data-stu-id="3bb98-107">Get</span></span>
```
Get-AzImportExportLocation -Name <String> [-AcceptLanguage <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="3bb98-108">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3bb98-108">GetViaIdentity</span></span>
```
Get-AzImportExportLocation -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3bb98-109">說明</span><span class="sxs-lookup"><span data-stu-id="3bb98-109">DESCRIPTION</span></span>
<span data-ttu-id="3bb98-110">傳回與匯入或匯出作業相關聯之磁片之位置的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3bb98-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="3bb98-111">位置是 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="3bb98-111">A location is an Azure region.</span></span>

## <span data-ttu-id="3bb98-112">示例</span><span class="sxs-lookup"><span data-stu-id="3bb98-112">EXAMPLES</span></span>

### <span data-ttu-id="3bb98-113">範例1：取得具有預設內容的所有 Azure 區域位置詳細資料</span><span class="sxs-lookup"><span data-stu-id="3bb98-113">Example 1: Get all Azure region location details with default context</span></span>
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

<span data-ttu-id="3bb98-114">這個 Cmdlet 會取得具有預設內容的所有 Azure 區域位置詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3bb98-114">This cmdlet gets all Azure region location details with default context.</span></span>

### <span data-ttu-id="3bb98-115">範例2：依位置名稱取得 Azure 地區位置詳細資料</span><span class="sxs-lookup"><span data-stu-id="3bb98-115">Example 2: Get Azure region location details by location name</span></span>
```powershell
PS C:\> Get-AzImportExportLocation -Name eastus
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="3bb98-116">這個 Cmdlet 透過位置名稱取得 Azure 區域位置詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3bb98-116">This cmdlet gets Azure region location details by location name.</span></span>

### <span data-ttu-id="3bb98-117">範例3：依身分識別取得 Azure 地區位置詳細資料</span><span class="sxs-lookup"><span data-stu-id="3bb98-117">Example 3: Get Azure region location details by identity</span></span>
```powershell
PS C:\> $Id = "/providers/Microsoft.ImportExport/locations/eastus"
PS C:\> Get-AzImportExportLocation -InputObject $Id
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="3bb98-118">這個 Cmdlet 清單會透過身分識別來取得 Azure 區域位置的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3bb98-118">This cmdlet lists gets Azure region location details by identity.</span></span>

## <span data-ttu-id="3bb98-119">參數</span><span class="sxs-lookup"><span data-stu-id="3bb98-119">PARAMETERS</span></span>

### <span data-ttu-id="3bb98-120">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="3bb98-120">-AcceptLanguage</span></span>
<span data-ttu-id="3bb98-121">指定回應的喜好語言。</span><span class="sxs-lookup"><span data-stu-id="3bb98-121">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="3bb98-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bb98-122">-DefaultProfile</span></span>
<span data-ttu-id="3bb98-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3bb98-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bb98-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3bb98-124">-InputObject</span></span>
<span data-ttu-id="3bb98-125">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3bb98-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3bb98-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="3bb98-126">-Name</span></span>
<span data-ttu-id="3bb98-127">位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="3bb98-127">The name of the location.</span></span>
<span data-ttu-id="3bb98-128">例如，美國西部或 westus。</span><span class="sxs-lookup"><span data-stu-id="3bb98-128">For example, West US or westus.</span></span>

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

### <span data-ttu-id="3bb98-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bb98-129">CommonParameters</span></span>
<span data-ttu-id="3bb98-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3bb98-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bb98-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3bb98-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bb98-132">輸入</span><span class="sxs-lookup"><span data-stu-id="3bb98-132">INPUTS</span></span>

### <span data-ttu-id="3bb98-133">IImportExportIdentity （ImportExport）的</span><span class="sxs-lookup"><span data-stu-id="3bb98-133">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="3bb98-134">輸出</span><span class="sxs-lookup"><span data-stu-id="3bb98-134">OUTPUTS</span></span>

### <span data-ttu-id="3bb98-135">ILocation （ImportExport）。 Api20161101。</span><span class="sxs-lookup"><span data-stu-id="3bb98-135">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation</span></span>

## <span data-ttu-id="3bb98-136">筆記</span><span class="sxs-lookup"><span data-stu-id="3bb98-136">NOTES</span></span>

<span data-ttu-id="3bb98-137">別名</span><span class="sxs-lookup"><span data-stu-id="3bb98-137">ALIASES</span></span>

<span data-ttu-id="3bb98-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="3bb98-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3bb98-139">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="3bb98-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3bb98-140">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="3bb98-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3bb98-141">INPUTOBJECT <IImportExportIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="3bb98-141">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3bb98-142">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="3bb98-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3bb98-143">`[JobName <String>]`：匯入/匯出作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="3bb98-143">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="3bb98-144">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="3bb98-144">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="3bb98-145">例如，美國西部或 westus。</span><span class="sxs-lookup"><span data-stu-id="3bb98-145">For example, West US or westus.</span></span>
  - <span data-ttu-id="3bb98-146">`[ResourceGroupName <String>]`：資源群組名稱會唯一識別使用者訂閱中的資源群組。</span><span class="sxs-lookup"><span data-stu-id="3bb98-146">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="3bb98-147">`[SubscriptionId <String>]`： Azure 使用者的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="3bb98-147">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="3bb98-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="3bb98-148">RELATED LINKS</span></span>

