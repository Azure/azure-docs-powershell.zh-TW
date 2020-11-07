---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstoragesettings
schema: 2.0.0
ms.openlocfilehash: 3ad33f83a4e8f96124682bbb189f210f813ead25
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966728"
---
# <span data-ttu-id="74397-101">Get-AzsStorageSettings</span><span class="sxs-lookup"><span data-stu-id="74397-101">Get-AzsStorageSettings</span></span>

## <span data-ttu-id="74397-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74397-102">SYNOPSIS</span></span>
<span data-ttu-id="74397-103">返回儲存資源提供者設定。</span><span class="sxs-lookup"><span data-stu-id="74397-103">Returns the storage resource provider settings.</span></span>

## <span data-ttu-id="74397-104">句法</span><span class="sxs-lookup"><span data-stu-id="74397-104">SYNTAX</span></span>

```
Get-AzsStorageSettings [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="74397-105">說明</span><span class="sxs-lookup"><span data-stu-id="74397-105">DESCRIPTION</span></span>
<span data-ttu-id="74397-106">返回儲存資源提供者設定。</span><span class="sxs-lookup"><span data-stu-id="74397-106">Returns the storage resource provider settings.</span></span>

## <span data-ttu-id="74397-107">示例</span><span class="sxs-lookup"><span data-stu-id="74397-107">EXAMPLES</span></span>

### <span data-ttu-id="74397-108">範例1：</span><span class="sxs-lookup"><span data-stu-id="74397-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageSettings
```

<span data-ttu-id="74397-109">取得儲存設定。</span><span class="sxs-lookup"><span data-stu-id="74397-109">Get the storage settings.</span></span>

## <span data-ttu-id="74397-110">參數</span><span class="sxs-lookup"><span data-stu-id="74397-110">PARAMETERS</span></span>

### <span data-ttu-id="74397-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74397-111">-DefaultProfile</span></span>
<span data-ttu-id="74397-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="74397-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74397-113">-位置</span><span class="sxs-lookup"><span data-stu-id="74397-113">-Location</span></span>
<span data-ttu-id="74397-114">資源位置。</span><span class="sxs-lookup"><span data-stu-id="74397-114">Resource location.</span></span>

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

### <span data-ttu-id="74397-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="74397-115">-SubscriptionId</span></span>
<span data-ttu-id="74397-116">訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="74397-116">Subscription Id.</span></span>

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

### <span data-ttu-id="74397-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74397-117">CommonParameters</span></span>
<span data-ttu-id="74397-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74397-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74397-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="74397-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74397-120">輸入</span><span class="sxs-lookup"><span data-stu-id="74397-120">INPUTS</span></span>

## <span data-ttu-id="74397-121">輸出</span><span class="sxs-lookup"><span data-stu-id="74397-121">OUTPUTS</span></span>

### <span data-ttu-id="74397-122">ISettings （StorageAdmin）。 Api201908Preview。</span><span class="sxs-lookup"><span data-stu-id="74397-122">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.ISettings</span></span>



## <span data-ttu-id="74397-123">筆記</span><span class="sxs-lookup"><span data-stu-id="74397-123">NOTES</span></span>

## <span data-ttu-id="74397-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="74397-124">RELATED LINKS</span></span>

