---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstoragesettings
schema: 2.0.0
ms.openlocfilehash: 3ad33f83a4e8f96124682bbb189f210f813ead25
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968197"
---
# <span data-ttu-id="5b18c-101">Get-AzsStorageSettings</span><span class="sxs-lookup"><span data-stu-id="5b18c-101">Get-AzsStorageSettings</span></span>

## <span data-ttu-id="5b18c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5b18c-102">SYNOPSIS</span></span>
<span data-ttu-id="5b18c-103">返回儲存資源提供者設定。</span><span class="sxs-lookup"><span data-stu-id="5b18c-103">Returns the storage resource provider settings.</span></span>

## <span data-ttu-id="5b18c-104">句法</span><span class="sxs-lookup"><span data-stu-id="5b18c-104">SYNTAX</span></span>

```
Get-AzsStorageSettings [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b18c-105">說明</span><span class="sxs-lookup"><span data-stu-id="5b18c-105">DESCRIPTION</span></span>
<span data-ttu-id="5b18c-106">返回儲存資源提供者設定。</span><span class="sxs-lookup"><span data-stu-id="5b18c-106">Returns the storage resource provider settings.</span></span>

## <span data-ttu-id="5b18c-107">示例</span><span class="sxs-lookup"><span data-stu-id="5b18c-107">EXAMPLES</span></span>

### <span data-ttu-id="5b18c-108">範例1：</span><span class="sxs-lookup"><span data-stu-id="5b18c-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageSettings
```

<span data-ttu-id="5b18c-109">取得儲存設定。</span><span class="sxs-lookup"><span data-stu-id="5b18c-109">Get the storage settings.</span></span>

## <span data-ttu-id="5b18c-110">參數</span><span class="sxs-lookup"><span data-stu-id="5b18c-110">PARAMETERS</span></span>

### <span data-ttu-id="5b18c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b18c-111">-DefaultProfile</span></span>
<span data-ttu-id="5b18c-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5b18c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b18c-113">-位置</span><span class="sxs-lookup"><span data-stu-id="5b18c-113">-Location</span></span>
<span data-ttu-id="5b18c-114">資源位置。</span><span class="sxs-lookup"><span data-stu-id="5b18c-114">Resource location.</span></span>

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

### <span data-ttu-id="5b18c-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5b18c-115">-SubscriptionId</span></span>
<span data-ttu-id="5b18c-116">訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="5b18c-116">Subscription Id.</span></span>

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

### <span data-ttu-id="5b18c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b18c-117">CommonParameters</span></span>
<span data-ttu-id="5b18c-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5b18c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b18c-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5b18c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b18c-120">輸入</span><span class="sxs-lookup"><span data-stu-id="5b18c-120">INPUTS</span></span>

## <span data-ttu-id="5b18c-121">輸出</span><span class="sxs-lookup"><span data-stu-id="5b18c-121">OUTPUTS</span></span>

### <span data-ttu-id="5b18c-122">ISettings （StorageAdmin）。 Api201908Preview。</span><span class="sxs-lookup"><span data-stu-id="5b18c-122">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.ISettings</span></span>



## <span data-ttu-id="5b18c-123">筆記</span><span class="sxs-lookup"><span data-stu-id="5b18c-123">NOTES</span></span>

## <span data-ttu-id="5b18c-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b18c-124">RELATED LINKS</span></span>

