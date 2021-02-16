---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
ms.openlocfilehash: b3bb193b47acf0f77851e5b9f4549d455a568b15
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138914"
---
# <span data-ttu-id="877c3-101">Get-AzSmartGroup</span><span class="sxs-lookup"><span data-stu-id="877c3-101">Get-AzSmartGroup</span></span>

## <span data-ttu-id="877c3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="877c3-102">SYNOPSIS</span></span>
<span data-ttu-id="877c3-103">取得智慧群組資訊</span><span class="sxs-lookup"><span data-stu-id="877c3-103">Gets Smart Groups information</span></span>

## <span data-ttu-id="877c3-104">句法</span><span class="sxs-lookup"><span data-stu-id="877c3-104">SYNTAX</span></span>

### <span data-ttu-id="877c3-105">SmartGroupsListByFilter (預設) </span><span class="sxs-lookup"><span data-stu-id="877c3-105">SmartGroupsListByFilter (Default)</span></span>
```
Get-AzSmartGroup [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="877c3-106">SmartGroupById</span><span class="sxs-lookup"><span data-stu-id="877c3-106">SmartGroupById</span></span>
```
Get-AzSmartGroup -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="877c3-107">說明</span><span class="sxs-lookup"><span data-stu-id="877c3-107">DESCRIPTION</span></span>
<span data-ttu-id="877c3-108">**AzSmartGroup** Cmdlet 會取得智慧群組資訊。</span><span class="sxs-lookup"><span data-stu-id="877c3-108">**Get-AzSmartGroup** cmdlet gets smart groups information.</span></span>

## <span data-ttu-id="877c3-109">示例</span><span class="sxs-lookup"><span data-stu-id="877c3-109">EXAMPLES</span></span>

### <span data-ttu-id="877c3-110">範例1</span><span class="sxs-lookup"><span data-stu-id="877c3-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroup -TimeRange "1h"
```

<span data-ttu-id="877c3-111">列出過去1小時內所形成的所有智慧群組。</span><span class="sxs-lookup"><span data-stu-id="877c3-111">List all smart groups formed in last 1 hour.</span></span> <span data-ttu-id="877c3-112">使用 Format-List 來取得清單中每個智慧群組的完整詳細資料。</span><span class="sxs-lookup"><span data-stu-id="877c3-112">Use Format-List to get the complete details of each smart group in list.</span></span>

### <span data-ttu-id="877c3-113">範例2</span><span class="sxs-lookup"><span data-stu-id="877c3-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSmartGroup -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="877c3-114">透過識別碼來取得智慧群組詳細資料 (GUID) 或資源識別碼 (完整的 ARM Id) </span><span class="sxs-lookup"><span data-stu-id="877c3-114">Get Smart Group details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="877c3-115">參數</span><span class="sxs-lookup"><span data-stu-id="877c3-115">PARAMETERS</span></span>

### <span data-ttu-id="877c3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="877c3-116">-DefaultProfile</span></span>
<span data-ttu-id="877c3-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="877c3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="877c3-118">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="877c3-118">-SmartGroupId</span></span>
<span data-ttu-id="877c3-119">SmartGroup 的 SmartGroup/ResourceId 的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="877c3-119">Unique Identifier of SmartGroup / ResourceId of SmartGroup.</span></span>

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

### <span data-ttu-id="877c3-120">-SortBy</span><span class="sxs-lookup"><span data-stu-id="877c3-120">-SortBy</span></span>
<span data-ttu-id="877c3-121">排序時要使用的警示屬性</span><span class="sxs-lookup"><span data-stu-id="877c3-121">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="877c3-122">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="877c3-122">-SortOrder</span></span>
<span data-ttu-id="877c3-123">排序次序</span><span class="sxs-lookup"><span data-stu-id="877c3-123">Sort Order</span></span>

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

### <span data-ttu-id="877c3-124">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="877c3-124">-TimeRange</span></span>
<span data-ttu-id="877c3-125">支援的時間範圍值-1h、1d、7d、30d (預設為 1d) </span><span class="sxs-lookup"><span data-stu-id="877c3-125">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="877c3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="877c3-126">CommonParameters</span></span>
<span data-ttu-id="877c3-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="877c3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="877c3-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="877c3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="877c3-129">輸入</span><span class="sxs-lookup"><span data-stu-id="877c3-129">INPUTS</span></span>

### <span data-ttu-id="877c3-130">所有</span><span class="sxs-lookup"><span data-stu-id="877c3-130">None</span></span>

## <span data-ttu-id="877c3-131">輸出</span><span class="sxs-lookup"><span data-stu-id="877c3-131">OUTPUTS</span></span>

### <span data-ttu-id="877c3-132">AlertsManagement. OutputModels. PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="877c3-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="877c3-133">筆記</span><span class="sxs-lookup"><span data-stu-id="877c3-133">NOTES</span></span>

## <span data-ttu-id="877c3-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="877c3-134">RELATED LINKS</span></span>
