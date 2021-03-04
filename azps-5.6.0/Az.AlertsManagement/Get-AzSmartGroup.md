---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/get-azsmartgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
ms.openlocfilehash: 52060a4d7624981ee29749c4f0dba3cc8a38fda5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912950"
---
# <span data-ttu-id="eec8e-101">Get-AzSmartGroup</span><span class="sxs-lookup"><span data-stu-id="eec8e-101">Get-AzSmartGroup</span></span>

## <span data-ttu-id="eec8e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eec8e-102">SYNOPSIS</span></span>
<span data-ttu-id="eec8e-103">獲得智慧群組資訊</span><span class="sxs-lookup"><span data-stu-id="eec8e-103">Gets Smart Groups information</span></span>

## <span data-ttu-id="eec8e-104">語法</span><span class="sxs-lookup"><span data-stu-id="eec8e-104">SYNTAX</span></span>

### <span data-ttu-id="eec8e-105">SmartGroupsListByFilter (預設) </span><span class="sxs-lookup"><span data-stu-id="eec8e-105">SmartGroupsListByFilter (Default)</span></span>
```
Get-AzSmartGroup [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eec8e-106">SmartGroupById</span><span class="sxs-lookup"><span data-stu-id="eec8e-106">SmartGroupById</span></span>
```
Get-AzSmartGroup -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eec8e-107">描述</span><span class="sxs-lookup"><span data-stu-id="eec8e-107">DESCRIPTION</span></span>
<span data-ttu-id="eec8e-108">**Get-AzSmartGroup** Cmdlet 會取得智慧型群組資訊。</span><span class="sxs-lookup"><span data-stu-id="eec8e-108">**Get-AzSmartGroup** cmdlet gets smart groups information.</span></span>

## <span data-ttu-id="eec8e-109">例子</span><span class="sxs-lookup"><span data-stu-id="eec8e-109">EXAMPLES</span></span>

### <span data-ttu-id="eec8e-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="eec8e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroup -TimeRange "1h"
```

<span data-ttu-id="eec8e-111">列出過去 1 小時內形成的所有智慧型群組。</span><span class="sxs-lookup"><span data-stu-id="eec8e-111">List all smart groups formed in last 1 hour.</span></span> <span data-ttu-id="eec8e-112">使用Format-List取得清單中每個智慧群組的完整詳細資料。</span><span class="sxs-lookup"><span data-stu-id="eec8e-112">Use Format-List to get the complete details of each smart group in list.</span></span>

### <span data-ttu-id="eec8e-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="eec8e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSmartGroup -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="eec8e-114">取得智慧群組詳細資料， (GUID) 或資源識別碼 (ARM 識別碼) </span><span class="sxs-lookup"><span data-stu-id="eec8e-114">Get Smart Group details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="eec8e-115">參數</span><span class="sxs-lookup"><span data-stu-id="eec8e-115">PARAMETERS</span></span>

### <span data-ttu-id="eec8e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eec8e-116">-DefaultProfile</span></span>
<span data-ttu-id="eec8e-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="eec8e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eec8e-118">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="eec8e-118">-SmartGroupId</span></span>
<span data-ttu-id="eec8e-119">SmartGroup / ResourceId 的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="eec8e-119">Unique Identifier of SmartGroup / ResourceId of SmartGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eec8e-120">-SortBy</span><span class="sxs-lookup"><span data-stu-id="eec8e-120">-SortBy</span></span>
<span data-ttu-id="eec8e-121">排序時要使用的警示屬性</span><span class="sxs-lookup"><span data-stu-id="eec8e-121">Alert property to use while sorting</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eec8e-122">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="eec8e-122">-SortOrder</span></span>
<span data-ttu-id="eec8e-123">排序次序</span><span class="sxs-lookup"><span data-stu-id="eec8e-123">Sort Order</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eec8e-124">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="eec8e-124">-TimeRange</span></span>
<span data-ttu-id="eec8e-125">支援的時間範圍值 - 1h、1d、7d、30d (預設值為 1d) </span><span class="sxs-lookup"><span data-stu-id="eec8e-125">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eec8e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eec8e-126">CommonParameters</span></span>
<span data-ttu-id="eec8e-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eec8e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eec8e-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eec8e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eec8e-129">輸入</span><span class="sxs-lookup"><span data-stu-id="eec8e-129">INPUTS</span></span>

### <span data-ttu-id="eec8e-130">沒有</span><span class="sxs-lookup"><span data-stu-id="eec8e-130">None</span></span>

## <span data-ttu-id="eec8e-131">輸出</span><span class="sxs-lookup"><span data-stu-id="eec8e-131">OUTPUTS</span></span>

### <span data-ttu-id="eec8e-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="eec8e-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="eec8e-133">筆記</span><span class="sxs-lookup"><span data-stu-id="eec8e-133">NOTES</span></span>

## <span data-ttu-id="eec8e-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="eec8e-134">RELATED LINKS</span></span>
