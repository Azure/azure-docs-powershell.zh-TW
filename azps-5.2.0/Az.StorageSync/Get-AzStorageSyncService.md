---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
ms.openlocfilehash: ec446a92c96bd92d7a4af5610f00ff76dcd50b50
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283363"
---
# <span data-ttu-id="af3ee-101">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="af3ee-101">Get-AzStorageSyncService</span></span>

## <span data-ttu-id="af3ee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="af3ee-102">SYNOPSIS</span></span>
<span data-ttu-id="af3ee-103">這個命令會列出 [訂閱/資源群組] 的指定範圍內的所有儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="af3ee-103">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

## <span data-ttu-id="af3ee-104">句法</span><span class="sxs-lookup"><span data-stu-id="af3ee-104">SYNTAX</span></span>

### <span data-ttu-id="af3ee-105">ParentStringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="af3ee-105">ParentStringParameterSet (Default)</span></span>
```
Get-AzStorageSyncService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="af3ee-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="af3ee-106">StringParameterSet</span></span>
```
Get-AzStorageSyncService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af3ee-107">說明</span><span class="sxs-lookup"><span data-stu-id="af3ee-107">DESCRIPTION</span></span>
<span data-ttu-id="af3ee-108">這個命令會列出 [訂閱/資源群組] 的指定範圍內的所有儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="af3ee-108">This command lists all storage sync services within a given scope of subscription/resource group.</span></span> <span data-ttu-id="af3ee-109">您也可以使用它來列出每個儲存空間同步處理服務的屬性。</span><span class="sxs-lookup"><span data-stu-id="af3ee-109">It can be used to also list the attributes of each storage sync service.</span></span>

## <span data-ttu-id="af3ee-110">示例</span><span class="sxs-lookup"><span data-stu-id="af3ee-110">EXAMPLES</span></span>

### <span data-ttu-id="af3ee-111">範例1</span><span class="sxs-lookup"><span data-stu-id="af3ee-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncService -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="af3ee-112">這個命令會列出指定資源群組內的所有儲存同步處理服務資源。</span><span class="sxs-lookup"><span data-stu-id="af3ee-112">This command lists all storage sync service resources within a given resource group.</span></span> <span data-ttu-id="af3ee-113">您也可以使用它來列出每個儲存空間同步處理服務的屬性。</span><span class="sxs-lookup"><span data-stu-id="af3ee-113">It can be used to also list the attributes of each storage sync service.</span></span> <span data-ttu-id="af3ee-114">指定-StorageSyncServiceName 以傳回特定的專案。</span><span class="sxs-lookup"><span data-stu-id="af3ee-114">Specify -StorageSyncServiceName to return a specific one.</span></span>

## <span data-ttu-id="af3ee-115">參數</span><span class="sxs-lookup"><span data-stu-id="af3ee-115">PARAMETERS</span></span>

### <span data-ttu-id="af3ee-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af3ee-116">-DefaultProfile</span></span>
<span data-ttu-id="af3ee-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="af3ee-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af3ee-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="af3ee-118">-Name</span></span>
<span data-ttu-id="af3ee-119">儲存空間同步處理服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="af3ee-119">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="af3ee-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af3ee-120">-ResourceGroupName</span></span>
<span data-ttu-id="af3ee-121">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="af3ee-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="af3ee-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af3ee-122">CommonParameters</span></span>
<span data-ttu-id="af3ee-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="af3ee-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af3ee-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="af3ee-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af3ee-125">輸入</span><span class="sxs-lookup"><span data-stu-id="af3ee-125">INPUTS</span></span>

### <span data-ttu-id="af3ee-126">System.object</span><span class="sxs-lookup"><span data-stu-id="af3ee-126">System.String</span></span>

## <span data-ttu-id="af3ee-127">輸出</span><span class="sxs-lookup"><span data-stu-id="af3ee-127">OUTPUTS</span></span>

### <span data-ttu-id="af3ee-128">PSStorageSyncService 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="af3ee-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="af3ee-129">筆記</span><span class="sxs-lookup"><span data-stu-id="af3ee-129">NOTES</span></span>

## <span data-ttu-id="af3ee-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="af3ee-130">RELATED LINKS</span></span>
