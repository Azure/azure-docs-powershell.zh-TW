---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharesynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
ms.openlocfilehash: a4d3adbcc63eda80bced31523a43cbbad4513205
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911709"
---
# <span data-ttu-id="8909b-101">Get-AzDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="8909b-101">Get-AzDataShareSynchronization</span></span>

## <span data-ttu-id="8909b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8909b-102">SYNOPSIS</span></span>
<span data-ttu-id="8909b-103">瞭解共用同步處理設定的資訊。</span><span class="sxs-lookup"><span data-stu-id="8909b-103">Gets information about synchronization setting for a share.</span></span>

## <span data-ttu-id="8909b-104">語法</span><span class="sxs-lookup"><span data-stu-id="8909b-104">SYNTAX</span></span>

### <span data-ttu-id="8909b-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8909b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronization -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8909b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8909b-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8909b-107">描述</span><span class="sxs-lookup"><span data-stu-id="8909b-107">DESCRIPTION</span></span>
<span data-ttu-id="8909b-108">**Get-AzDataShareSynchrononization** Cmdlet 提供有關資料共用帳戶下共用中所有同步處理設定的資訊。</span><span class="sxs-lookup"><span data-stu-id="8909b-108">The **Get-AzDataShareSynchronization** cmdlet provides information about all the synchronization setting present in a share under a data share account.</span></span>

## <span data-ttu-id="8909b-109">例子</span><span class="sxs-lookup"><span data-stu-id="8909b-109">EXAMPLES</span></span>

### <span data-ttu-id="8909b-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="8909b-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare"

Company           : ADS Test
DurationMs        : 107013
EndTime           : 7/8/2019 11:53:18 PM
Message           :
StartTime         : 7/8/2019 11:51:34 PM
Status            : Succeeded
SynchronizationId : e6dc7080-6589-4628-8b50-8fc31b460089
```

<span data-ttu-id="8909b-111">這個命令會提供資料共用帳戶 WikiAds 中 Share AdsShare 中所有同步處理設定的資訊。</span><span class="sxs-lookup"><span data-stu-id="8909b-111">This commands provides information about all synchronization settings present in share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="8909b-112">參數</span><span class="sxs-lookup"><span data-stu-id="8909b-112">PARAMETERS</span></span>

### <span data-ttu-id="8909b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8909b-113">-AccountName</span></span>
<span data-ttu-id="8909b-114">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="8909b-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8909b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8909b-115">-DefaultProfile</span></span>
<span data-ttu-id="8909b-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8909b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8909b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8909b-117">-ResourceGroupName</span></span>
<span data-ttu-id="8909b-118">Azure 資料共用帳戶的資源組名</span><span class="sxs-lookup"><span data-stu-id="8909b-118">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8909b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8909b-119">-ResourceId</span></span>
<span data-ttu-id="8909b-120">Azure 資料共用資源識別碼</span><span class="sxs-lookup"><span data-stu-id="8909b-120">Azure data share resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8909b-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="8909b-121">-ShareName</span></span>
<span data-ttu-id="8909b-122">Azure 資料共用名稱</span><span class="sxs-lookup"><span data-stu-id="8909b-122">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8909b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8909b-123">CommonParameters</span></span>
<span data-ttu-id="8909b-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8909b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8909b-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8909b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8909b-126">輸入</span><span class="sxs-lookup"><span data-stu-id="8909b-126">INPUTS</span></span>

### <span data-ttu-id="8909b-127">System.String</span><span class="sxs-lookup"><span data-stu-id="8909b-127">System.String</span></span>

## <span data-ttu-id="8909b-128">輸出</span><span class="sxs-lookup"><span data-stu-id="8909b-128">OUTPUTS</span></span>

### <span data-ttu-id="8909b-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDShareSynchrononization</span><span class="sxs-lookup"><span data-stu-id="8909b-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span></span>

## <span data-ttu-id="8909b-130">筆記</span><span class="sxs-lookup"><span data-stu-id="8909b-130">NOTES</span></span>

## <span data-ttu-id="8909b-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="8909b-131">RELATED LINKS</span></span>
