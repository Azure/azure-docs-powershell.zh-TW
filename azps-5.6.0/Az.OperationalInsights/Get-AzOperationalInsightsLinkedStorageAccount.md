---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5ae174f31cdbe23a28dd9a21b44b640239e78fdd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908046"
---
# <span data-ttu-id="7b068-101">Get-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7b068-101">Get-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="7b068-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7b068-102">SYNOPSIS</span></span>
<span data-ttu-id="7b068-103">取得或列出連結的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="7b068-103">Get or list linked storage account</span></span>

## <span data-ttu-id="7b068-104">語法</span><span class="sxs-lookup"><span data-stu-id="7b068-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b068-105">描述</span><span class="sxs-lookup"><span data-stu-id="7b068-105">DESCRIPTION</span></span>
<span data-ttu-id="7b068-106">取得連結的儲存空間帳戶，在未指定 "-DataSourceType" 時列出所有連結的儲存帳戶</span><span class="sxs-lookup"><span data-stu-id="7b068-106">Get linked storage account, list all linked storage accounts when "-DataSourceType" was not specified</span></span>

## <span data-ttu-id="7b068-107">例子</span><span class="sxs-lookup"><span data-stu-id="7b068-107">EXAMPLES</span></span>

### <span data-ttu-id="7b068-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="7b068-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name}

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/customlogs
Name              :
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{account}}
```

<span data-ttu-id="7b068-109">列出工作區 {workspace-name} 的連結儲存空間需求</span><span class="sxs-lookup"><span data-stu-id="7b068-109">list linked storage accoounts for workspace {workspace-name}</span></span>

## <span data-ttu-id="7b068-110">參數</span><span class="sxs-lookup"><span data-stu-id="7b068-110">PARAMETERS</span></span>

### <span data-ttu-id="7b068-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="7b068-111">-DataSourceType</span></span>
<span data-ttu-id="7b068-112">資料來源類型應該是其中一個'CustomLogs'，'AzureWatson'。</span><span class="sxs-lookup"><span data-stu-id="7b068-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="7b068-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b068-113">-DefaultProfile</span></span>
<span data-ttu-id="7b068-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7b068-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b068-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b068-115">-ResourceGroupName</span></span>
<span data-ttu-id="7b068-116">資源組名。</span><span class="sxs-lookup"><span data-stu-id="7b068-116">The resource group name.</span></span>

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

### <span data-ttu-id="7b068-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7b068-117">-WorkspaceName</span></span>
<span data-ttu-id="7b068-118">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="7b068-118">The workspace name.</span></span>

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

### <span data-ttu-id="7b068-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b068-119">CommonParameters</span></span>
<span data-ttu-id="7b068-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7b068-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b068-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7b068-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b068-122">輸入</span><span class="sxs-lookup"><span data-stu-id="7b068-122">INPUTS</span></span>

### <span data-ttu-id="7b068-123">System.String</span><span class="sxs-lookup"><span data-stu-id="7b068-123">System.String</span></span>

## <span data-ttu-id="7b068-124">輸出</span><span class="sxs-lookup"><span data-stu-id="7b068-124">OUTPUTS</span></span>

### <span data-ttu-id="7b068-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="7b068-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="7b068-126">筆記</span><span class="sxs-lookup"><span data-stu-id="7b068-126">NOTES</span></span>

## <span data-ttu-id="7b068-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="7b068-127">RELATED LINKS</span></span>