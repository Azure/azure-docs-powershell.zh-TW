---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5095a3d9f989a6600776140239b9207ba3293d53
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98450066"
---
# <span data-ttu-id="af36d-101">Get-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="af36d-101">Get-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="af36d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="af36d-102">SYNOPSIS</span></span>
<span data-ttu-id="af36d-103">取得或列出連結的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="af36d-103">Get or list linked storage account</span></span>

## <span data-ttu-id="af36d-104">句法</span><span class="sxs-lookup"><span data-stu-id="af36d-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af36d-105">說明</span><span class="sxs-lookup"><span data-stu-id="af36d-105">DESCRIPTION</span></span>
<span data-ttu-id="af36d-106">[取得連結的儲存空間帳戶]，在未指定 [-DataSourceType] 時列出所有連結的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="af36d-106">Get linked storage account, list all linked storage accounts when "-DataSourceType" was not specified</span></span>

## <span data-ttu-id="af36d-107">示例</span><span class="sxs-lookup"><span data-stu-id="af36d-107">EXAMPLES</span></span>

### <span data-ttu-id="af36d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="af36d-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name}

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/customlogs
Name              :
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{account}}
```

<span data-ttu-id="af36d-109">清單中的 [連結儲存空間] accoounts 工作區 {工作區 {名稱}</span><span class="sxs-lookup"><span data-stu-id="af36d-109">list linked storage accoounts for workspace {workspace-name}</span></span>

## <span data-ttu-id="af36d-110">參數</span><span class="sxs-lookup"><span data-stu-id="af36d-110">PARAMETERS</span></span>

### <span data-ttu-id="af36d-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="af36d-111">-DataSourceType</span></span>
<span data-ttu-id="af36d-112">資料來源類型應該是 "CustomLogs"、"AzureWatson"。</span><span class="sxs-lookup"><span data-stu-id="af36d-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CustomLogs, AzureWatson

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af36d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af36d-113">-DefaultProfile</span></span>
<span data-ttu-id="af36d-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="af36d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af36d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af36d-115">-ResourceGroupName</span></span>
<span data-ttu-id="af36d-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="af36d-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af36d-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="af36d-117">-WorkspaceName</span></span>
<span data-ttu-id="af36d-118">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="af36d-118">The workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af36d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af36d-119">CommonParameters</span></span>
<span data-ttu-id="af36d-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="af36d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af36d-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="af36d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af36d-122">輸入</span><span class="sxs-lookup"><span data-stu-id="af36d-122">INPUTS</span></span>

### <span data-ttu-id="af36d-123">System.object</span><span class="sxs-lookup"><span data-stu-id="af36d-123">System.String</span></span>

## <span data-ttu-id="af36d-124">輸出</span><span class="sxs-lookup"><span data-stu-id="af36d-124">OUTPUTS</span></span>

### <span data-ttu-id="af36d-125">PSLinkedStorageAccountsResource 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="af36d-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="af36d-126">筆記</span><span class="sxs-lookup"><span data-stu-id="af36d-126">NOTES</span></span>

## <span data-ttu-id="af36d-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="af36d-127">RELATED LINKS</span></span>