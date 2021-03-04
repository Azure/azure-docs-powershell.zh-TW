---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 55e887ed60eaf4dd4fc6c26423686b99572702ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916150"
---
# <span data-ttu-id="eef59-101">Get-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="eef59-101">Get-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="eef59-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eef59-102">SYNOPSIS</span></span>
<span data-ttu-id="eef59-103">在共用上獲得同步處理設定相關資訊。</span><span class="sxs-lookup"><span data-stu-id="eef59-103">Gets information about synchronization setting on a share.</span></span>

## <span data-ttu-id="eef59-104">語法</span><span class="sxs-lookup"><span data-stu-id="eef59-104">SYNTAX</span></span>

### <span data-ttu-id="eef59-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="eef59-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eef59-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eef59-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eef59-107">描述</span><span class="sxs-lookup"><span data-stu-id="eef59-107">DESCRIPTION</span></span>
<span data-ttu-id="eef59-108">**Get-AzDataShareSynchronizationSetting** Cmdlet 提供共用上啟用同步處理的資訊。</span><span class="sxs-lookup"><span data-stu-id="eef59-108">The **Get-AzDataShareSynchronizationSetting** cmdlet provides information about synchronization enabled on a share.</span></span> 

## <span data-ttu-id="eef59-109">例子</span><span class="sxs-lookup"><span data-stu-id="eef59-109">EXAMPLES</span></span>

### <span data-ttu-id="eef59-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="eef59-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ShareSynchronization"

RecurrenceInterval  : Day
SynchronizationTime : 7/9/2019 9:00:00 AM
ProvisioningState   : Succeeded
CreatedAt           : 7/10/2019 12:01:08 AM
CreatedBy           : ADS Test
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.
                      DataShare/accounts/WikiAds/shares/AdShare/synchronizationSettings/ShareSynchronization
Name                : ShareSynchronization
Type                : Microsoft.DataShare/SynchronizationSettings
```

<span data-ttu-id="eef59-111">此命令提供在資料共用帳戶 WikiAds 下的 Share AdsShare 上啟用同步處理 ShareSynchronization 的資訊。</span><span class="sxs-lookup"><span data-stu-id="eef59-111">This command provides information about synchronization ShareSynchronization enabled on share AdsShare under data share account WikiAds.</span></span>

## <span data-ttu-id="eef59-112">參數</span><span class="sxs-lookup"><span data-stu-id="eef59-112">PARAMETERS</span></span>

### <span data-ttu-id="eef59-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eef59-113">-AccountName</span></span>
<span data-ttu-id="eef59-114">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="eef59-114">Azure data share account name</span></span>

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

### <span data-ttu-id="eef59-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eef59-115">-DefaultProfile</span></span>
<span data-ttu-id="eef59-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="eef59-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eef59-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="eef59-117">-Name</span></span>
<span data-ttu-id="eef59-118">同步處理設定的名稱</span><span class="sxs-lookup"><span data-stu-id="eef59-118">Name for Synchronization Setting</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eef59-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eef59-119">-ResourceGroupName</span></span>
<span data-ttu-id="eef59-120">Azure 資料共用帳戶的資源組名</span><span class="sxs-lookup"><span data-stu-id="eef59-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="eef59-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eef59-121">-ResourceId</span></span>
<span data-ttu-id="eef59-122">Azure 資料共用同步處理設定的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="eef59-122">The resource id of the azure data share synchronization setting</span></span>

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

### <span data-ttu-id="eef59-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="eef59-123">-ShareName</span></span>
<span data-ttu-id="eef59-124">Azure 資料共用名稱</span><span class="sxs-lookup"><span data-stu-id="eef59-124">Azure data share name</span></span>

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

### <span data-ttu-id="eef59-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eef59-125">CommonParameters</span></span>
<span data-ttu-id="eef59-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eef59-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eef59-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eef59-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eef59-128">輸入</span><span class="sxs-lookup"><span data-stu-id="eef59-128">INPUTS</span></span>

### <span data-ttu-id="eef59-129">System.String</span><span class="sxs-lookup"><span data-stu-id="eef59-129">System.String</span></span>

## <span data-ttu-id="eef59-130">輸出</span><span class="sxs-lookup"><span data-stu-id="eef59-130">OUTPUTS</span></span>

### <span data-ttu-id="eef59-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="eef59-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="eef59-132">筆記</span><span class="sxs-lookup"><span data-stu-id="eef59-132">NOTES</span></span>

## <span data-ttu-id="eef59-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="eef59-133">RELATED LINKS</span></span>
