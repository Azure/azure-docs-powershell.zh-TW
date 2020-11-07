---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstoragesettings
schema: 2.0.0
ms.openlocfilehash: 3ad33f83a4e8f96124682bbb189f210f813ead25
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794855"
---
# <span data-ttu-id="2fef8-101">Get-AzsStorageSettings</span><span class="sxs-lookup"><span data-stu-id="2fef8-101">Get-AzsStorageSettings</span></span>

## <span data-ttu-id="2fef8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2fef8-102">SYNOPSIS</span></span>
<span data-ttu-id="2fef8-103">返回儲存資源提供者設定。</span><span class="sxs-lookup"><span data-stu-id="2fef8-103">Returns the storage resource provider settings.</span></span>

## <span data-ttu-id="2fef8-104">句法</span><span class="sxs-lookup"><span data-stu-id="2fef8-104">SYNTAX</span></span>

```
Get-AzsStorageSettings [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="2fef8-105">說明</span><span class="sxs-lookup"><span data-stu-id="2fef8-105">DESCRIPTION</span></span>
<span data-ttu-id="2fef8-106">返回儲存資源提供者設定。</span><span class="sxs-lookup"><span data-stu-id="2fef8-106">Returns the storage resource provider settings.</span></span>

## <span data-ttu-id="2fef8-107">示例</span><span class="sxs-lookup"><span data-stu-id="2fef8-107">EXAMPLES</span></span>

### <span data-ttu-id="2fef8-108">範例1：</span><span class="sxs-lookup"><span data-stu-id="2fef8-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageSettings
```

<span data-ttu-id="2fef8-109">取得儲存設定。</span><span class="sxs-lookup"><span data-stu-id="2fef8-109">Get the storage settings.</span></span>

## <span data-ttu-id="2fef8-110">參數</span><span class="sxs-lookup"><span data-stu-id="2fef8-110">PARAMETERS</span></span>

### <span data-ttu-id="2fef8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fef8-111">-DefaultProfile</span></span>
<span data-ttu-id="2fef8-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2fef8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2fef8-113">-位置</span><span class="sxs-lookup"><span data-stu-id="2fef8-113">-Location</span></span>
<span data-ttu-id="2fef8-114">資源位置。</span><span class="sxs-lookup"><span data-stu-id="2fef8-114">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2fef8-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2fef8-115">-SubscriptionId</span></span>
<span data-ttu-id="2fef8-116">訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="2fef8-116">Subscription Id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2fef8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fef8-117">CommonParameters</span></span>
<span data-ttu-id="2fef8-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2fef8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fef8-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2fef8-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fef8-120">輸入</span><span class="sxs-lookup"><span data-stu-id="2fef8-120">INPUTS</span></span>

## <span data-ttu-id="2fef8-121">輸出</span><span class="sxs-lookup"><span data-stu-id="2fef8-121">OUTPUTS</span></span>

### <span data-ttu-id="2fef8-122">ISettings （StorageAdmin）。 Api201908Preview。</span><span class="sxs-lookup"><span data-stu-id="2fef8-122">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.ISettings</span></span>



## <span data-ttu-id="2fef8-123">筆記</span><span class="sxs-lookup"><span data-stu-id="2fef8-123">NOTES</span></span>

## <span data-ttu-id="2fef8-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="2fef8-124">RELATED LINKS</span></span>

