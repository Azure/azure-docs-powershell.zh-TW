---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
ms.openlocfilehash: c724527b380e0004d30e0790024634bcc6ce550d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614443"
---
# <span data-ttu-id="23024-101">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="23024-101">Get-AzStorageSyncService</span></span>

## <span data-ttu-id="23024-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23024-102">SYNOPSIS</span></span>
<span data-ttu-id="23024-103">這個命令會列出 [訂閱/資源群組] 的指定範圍內的所有儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="23024-103">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

## <span data-ttu-id="23024-104">句法</span><span class="sxs-lookup"><span data-stu-id="23024-104">SYNTAX</span></span>

### <span data-ttu-id="23024-105">ParentStringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="23024-105">ParentStringParameterSet (Default)</span></span>
```
Get-AzStorageSyncService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23024-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="23024-106">StringParameterSet</span></span>
```
Get-AzStorageSyncService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23024-107">說明</span><span class="sxs-lookup"><span data-stu-id="23024-107">DESCRIPTION</span></span>
<span data-ttu-id="23024-108">這個命令會列出 [訂閱/資源群組] 的指定範圍內的所有儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="23024-108">This command lists all storage sync services within a given scope of subscription/resource group.</span></span> <span data-ttu-id="23024-109">您也可以使用它來列出每個儲存空間同步處理服務的屬性。</span><span class="sxs-lookup"><span data-stu-id="23024-109">It can be used to also list the attributes of each storage sync service.</span></span>

## <span data-ttu-id="23024-110">示例</span><span class="sxs-lookup"><span data-stu-id="23024-110">EXAMPLES</span></span>

### <span data-ttu-id="23024-111">範例1</span><span class="sxs-lookup"><span data-stu-id="23024-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncService -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="23024-112">這個命令會列出指定資源群組內的所有儲存同步處理服務資源。</span><span class="sxs-lookup"><span data-stu-id="23024-112">This command lists all storage sync service resources within a given resource group.</span></span> <span data-ttu-id="23024-113">您也可以使用它來列出每個儲存空間同步處理服務的屬性。</span><span class="sxs-lookup"><span data-stu-id="23024-113">It can be used to also list the attributes of each storage sync service.</span></span> <span data-ttu-id="23024-114">指定-StorageSyncServiceName 以傳回特定的專案。</span><span class="sxs-lookup"><span data-stu-id="23024-114">Specify -StorageSyncServiceName to return a specific one.</span></span>

## <span data-ttu-id="23024-115">參數</span><span class="sxs-lookup"><span data-stu-id="23024-115">PARAMETERS</span></span>

### <span data-ttu-id="23024-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23024-116">-DefaultProfile</span></span>
<span data-ttu-id="23024-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="23024-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23024-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="23024-118">-Name</span></span>
<span data-ttu-id="23024-119">儲存空間同步處理服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="23024-119">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="23024-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23024-120">-ResourceGroupName</span></span>
<span data-ttu-id="23024-121">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="23024-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="23024-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23024-122">CommonParameters</span></span>
<span data-ttu-id="23024-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23024-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23024-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="23024-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23024-125">輸入</span><span class="sxs-lookup"><span data-stu-id="23024-125">INPUTS</span></span>

### <span data-ttu-id="23024-126">System.object</span><span class="sxs-lookup"><span data-stu-id="23024-126">System.String</span></span>

## <span data-ttu-id="23024-127">輸出</span><span class="sxs-lookup"><span data-stu-id="23024-127">OUTPUTS</span></span>

### <span data-ttu-id="23024-128">PSStorageSyncService 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="23024-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="23024-129">筆記</span><span class="sxs-lookup"><span data-stu-id="23024-129">NOTES</span></span>

## <span data-ttu-id="23024-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="23024-130">RELATED LINKS</span></span>