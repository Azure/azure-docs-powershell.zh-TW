---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/get-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
ms.openlocfilehash: 3aa6c569eb7f67b6021f7f40059cc9e528355a51
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907202"
---
# <span data-ttu-id="2e312-101">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="2e312-101">Get-AzStorageSyncService</span></span>

## <span data-ttu-id="2e312-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2e312-102">SYNOPSIS</span></span>
<span data-ttu-id="2e312-103">此命令會列出訂閱/資源群組範圍內的所有儲存同步服務。</span><span class="sxs-lookup"><span data-stu-id="2e312-103">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

## <span data-ttu-id="2e312-104">語法</span><span class="sxs-lookup"><span data-stu-id="2e312-104">SYNTAX</span></span>

### <span data-ttu-id="2e312-105">ParentStringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2e312-105">ParentStringParameterSet (Default)</span></span>
```
Get-AzStorageSyncService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2e312-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e312-106">StringParameterSet</span></span>
```
Get-AzStorageSyncService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e312-107">描述</span><span class="sxs-lookup"><span data-stu-id="2e312-107">DESCRIPTION</span></span>
<span data-ttu-id="2e312-108">此命令會列出訂閱/資源群組範圍內的所有儲存同步服務。</span><span class="sxs-lookup"><span data-stu-id="2e312-108">This command lists all storage sync services within a given scope of subscription/resource group.</span></span> <span data-ttu-id="2e312-109">它可以用來列出每個儲存同步服務的屬性。</span><span class="sxs-lookup"><span data-stu-id="2e312-109">It can be used to also list the attributes of each storage sync service.</span></span>

## <span data-ttu-id="2e312-110">例子</span><span class="sxs-lookup"><span data-stu-id="2e312-110">EXAMPLES</span></span>

### <span data-ttu-id="2e312-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="2e312-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncService -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="2e312-112">此命令會列出給定資源群組內的所有儲存同步服務資源。</span><span class="sxs-lookup"><span data-stu-id="2e312-112">This command lists all storage sync service resources within a given resource group.</span></span> <span data-ttu-id="2e312-113">它可以用來列出每個儲存同步服務的屬性。</span><span class="sxs-lookup"><span data-stu-id="2e312-113">It can be used to also list the attributes of each storage sync service.</span></span> <span data-ttu-id="2e312-114">指定 -StorageSyncServiceName 以返回特定名稱。</span><span class="sxs-lookup"><span data-stu-id="2e312-114">Specify -StorageSyncServiceName to return a specific one.</span></span>

## <span data-ttu-id="2e312-115">參數</span><span class="sxs-lookup"><span data-stu-id="2e312-115">PARAMETERS</span></span>

### <span data-ttu-id="2e312-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e312-116">-DefaultProfile</span></span>
<span data-ttu-id="2e312-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2e312-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e312-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="2e312-118">-Name</span></span>
<span data-ttu-id="2e312-119">儲存空間同步服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="2e312-119">Name of the storage sync service.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: StorageSyncServiceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e312-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e312-120">-ResourceGroupName</span></span>
<span data-ttu-id="2e312-121">資源組名。</span><span class="sxs-lookup"><span data-stu-id="2e312-121">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e312-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e312-122">CommonParameters</span></span>
<span data-ttu-id="2e312-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2e312-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e312-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2e312-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e312-125">輸入</span><span class="sxs-lookup"><span data-stu-id="2e312-125">INPUTS</span></span>

### <span data-ttu-id="2e312-126">System.String</span><span class="sxs-lookup"><span data-stu-id="2e312-126">System.String</span></span>

## <span data-ttu-id="2e312-127">輸出</span><span class="sxs-lookup"><span data-stu-id="2e312-127">OUTPUTS</span></span>

### <span data-ttu-id="2e312-128">Microsoft.Azure.Commands.StorageSync.models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="2e312-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="2e312-129">筆記</span><span class="sxs-lookup"><span data-stu-id="2e312-129">NOTES</span></span>

## <span data-ttu-id="2e312-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="2e312-130">RELATED LINKS</span></span>
