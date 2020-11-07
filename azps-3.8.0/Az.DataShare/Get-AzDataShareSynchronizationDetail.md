---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
ms.openlocfilehash: 8e0f62f4b3d29d0aff9a2bdfcd7916805544af14
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797941"
---
# <span data-ttu-id="eff2f-101">Get-AzDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="eff2f-101">Get-AzDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="eff2f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eff2f-102">SYNOPSIS</span></span>
<span data-ttu-id="eff2f-103">取得共用的同步處理詳細資料的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="eff2f-103">Gets information about synchronization details for a share.</span></span>

## <span data-ttu-id="eff2f-104">句法</span><span class="sxs-lookup"><span data-stu-id="eff2f-104">SYNTAX</span></span>

### <span data-ttu-id="eff2f-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="eff2f-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationDetail -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eff2f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eff2f-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eff2f-107">說明</span><span class="sxs-lookup"><span data-stu-id="eff2f-107">DESCRIPTION</span></span>
<span data-ttu-id="eff2f-108">**AzDataShareSynchronizationDetail** Cmdlet 提供為共用啟動的同步處理的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="eff2f-108">The **Get-AzDataShareSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share.</span></span>

## <span data-ttu-id="eff2f-109">示例</span><span class="sxs-lookup"><span data-stu-id="eff2f-109">EXAMPLES</span></span>

### <span data-ttu-id="eff2f-110">範例1</span><span class="sxs-lookup"><span data-stu-id="eff2f-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronizationDetail -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -SynchronizationId "02a17faa-4498-45ee-a884-162180af9251"

DataSetId    : d2411889-5357-4ca8-8d65-9363e46ef2ed
DataSetType  : BlobFolder
EndTime      : 7/8/2019 10:24:27 PM
StartTime    : 7/8/2019 10:23:09 PM
Status       : Succeeded
DurationMs   : 78870
FilesRead    : 1
FilesWritten : 1
SizeRead     : 2779935
SizeWritten  : 2779935
Name         : 16d5161b-2b3f-4d90-b074-13ad7121bcc7
Message      :
```

<span data-ttu-id="eff2f-111">這個命令會提供與提供的同步處理識別碼相對應之所有資料集的同步處理詳細資料的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="eff2f-111">This command provides information about the synchronization details of all the data sets corresponding to the provided synchronization id.</span></span>

## <span data-ttu-id="eff2f-112">參數</span><span class="sxs-lookup"><span data-stu-id="eff2f-112">PARAMETERS</span></span>

### <span data-ttu-id="eff2f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eff2f-113">-AccountName</span></span>
<span data-ttu-id="eff2f-114">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="eff2f-114">Azure data share account name</span></span>

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

### <span data-ttu-id="eff2f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eff2f-115">-DefaultProfile</span></span>
<span data-ttu-id="eff2f-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eff2f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eff2f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eff2f-117">-ResourceGroupName</span></span>
<span data-ttu-id="eff2f-118">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="eff2f-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="eff2f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eff2f-119">-ResourceId</span></span>
<span data-ttu-id="eff2f-120">Azure 資料共用資源識別碼</span><span class="sxs-lookup"><span data-stu-id="eff2f-120">Azure data share resource id</span></span>

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

### <span data-ttu-id="eff2f-121">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="eff2f-121">-ShareName</span></span>
<span data-ttu-id="eff2f-122">Azure 資料共用名稱</span><span class="sxs-lookup"><span data-stu-id="eff2f-122">Azure data share name</span></span>

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

### <span data-ttu-id="eff2f-123">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="eff2f-123">-SynchronizationId</span></span>
<span data-ttu-id="eff2f-124">共用同步處理的同步處理 id</span><span class="sxs-lookup"><span data-stu-id="eff2f-124">Synchronization id of share synchronization</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eff2f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eff2f-125">CommonParameters</span></span>
<span data-ttu-id="eff2f-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eff2f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eff2f-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eff2f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eff2f-128">輸入</span><span class="sxs-lookup"><span data-stu-id="eff2f-128">INPUTS</span></span>

### <span data-ttu-id="eff2f-129">System.object</span><span class="sxs-lookup"><span data-stu-id="eff2f-129">System.String</span></span>

## <span data-ttu-id="eff2f-130">輸出</span><span class="sxs-lookup"><span data-stu-id="eff2f-130">OUTPUTS</span></span>

### <span data-ttu-id="eff2f-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="eff2f-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="eff2f-132">筆記</span><span class="sxs-lookup"><span data-stu-id="eff2f-132">NOTES</span></span>

## <span data-ttu-id="eff2f-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="eff2f-133">RELATED LINKS</span></span>
