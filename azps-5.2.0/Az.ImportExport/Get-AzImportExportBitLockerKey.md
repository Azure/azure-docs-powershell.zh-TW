---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportbitlockerkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
ms.openlocfilehash: 5f7a1fe5e8b80f6847bc3b3ca063d7166bf3ea95
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278219"
---
# <span data-ttu-id="9faa5-101">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="9faa5-101">Get-AzImportExportBitLockerKey</span></span>

## <span data-ttu-id="9faa5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9faa5-102">SYNOPSIS</span></span>
<span data-ttu-id="9faa5-103">傳回指定作業中所有磁片磁碟機的 BitLocker 金鑰。</span><span class="sxs-lookup"><span data-stu-id="9faa5-103">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="9faa5-104">句法</span><span class="sxs-lookup"><span data-stu-id="9faa5-104">SYNTAX</span></span>

```
Get-AzImportExportBitLockerKey -JobName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9faa5-105">說明</span><span class="sxs-lookup"><span data-stu-id="9faa5-105">DESCRIPTION</span></span>
<span data-ttu-id="9faa5-106">傳回指定作業中所有磁片磁碟機的 BitLocker 金鑰。</span><span class="sxs-lookup"><span data-stu-id="9faa5-106">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="9faa5-107">示例</span><span class="sxs-lookup"><span data-stu-id="9faa5-107">EXAMPLES</span></span>

### <span data-ttu-id="9faa5-108">範例1：列出指定 ImportExport 作業中的所有 BitLocker 金鑰</span><span class="sxs-lookup"><span data-stu-id="9faa5-108">Example 1: List all BitLocker Keys in specified ImportExport job</span></span>
```powershell
PS C:\> Get-AzImportExportBitLockerKey -JobName test-job -ResourceGroupName ImportTestRG 
BitLockerKey                                            DriveId
------------                                            -------
238810-662376-448998-450120-652806-203390-606320-483076 9CA995BA
```

<span data-ttu-id="9faa5-109">這個 Cmdlet 會列出指定 ImportExport 作業中的所有 BitLocker 金鑰。</span><span class="sxs-lookup"><span data-stu-id="9faa5-109">This cmdlet lists all BitLocker Keys in specified ImportExport job.</span></span>

## <span data-ttu-id="9faa5-110">參數</span><span class="sxs-lookup"><span data-stu-id="9faa5-110">PARAMETERS</span></span>

### <span data-ttu-id="9faa5-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="9faa5-111">-AcceptLanguage</span></span>
<span data-ttu-id="9faa5-112">指定回應的喜好語言。</span><span class="sxs-lookup"><span data-stu-id="9faa5-112">Specifies the preferred language for the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9faa5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9faa5-113">-DefaultProfile</span></span>
<span data-ttu-id="9faa5-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9faa5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9faa5-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="9faa5-115">-JobName</span></span>
<span data-ttu-id="9faa5-116">匯入/匯出作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="9faa5-116">The name of the import/export job.</span></span>

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

### <span data-ttu-id="9faa5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9faa5-117">-ResourceGroupName</span></span>
<span data-ttu-id="9faa5-118">資源群組名稱會唯一識別使用者訂閱中的資源群組。</span><span class="sxs-lookup"><span data-stu-id="9faa5-118">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="9faa5-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9faa5-119">-SubscriptionId</span></span>
<span data-ttu-id="9faa5-120">Azure 使用者的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="9faa5-120">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="9faa5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9faa5-121">CommonParameters</span></span>
<span data-ttu-id="9faa5-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9faa5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9faa5-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9faa5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9faa5-124">輸入</span><span class="sxs-lookup"><span data-stu-id="9faa5-124">INPUTS</span></span>

## <span data-ttu-id="9faa5-125">輸出</span><span class="sxs-lookup"><span data-stu-id="9faa5-125">OUTPUTS</span></span>

### <span data-ttu-id="9faa5-126">IDriveBitLockerKey （ImportExport）。 Api20161101。</span><span class="sxs-lookup"><span data-stu-id="9faa5-126">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveBitLockerKey</span></span>

## <span data-ttu-id="9faa5-127">筆記</span><span class="sxs-lookup"><span data-stu-id="9faa5-127">NOTES</span></span>

<span data-ttu-id="9faa5-128">別名</span><span class="sxs-lookup"><span data-stu-id="9faa5-128">ALIASES</span></span>

## <span data-ttu-id="9faa5-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="9faa5-129">RELATED LINKS</span></span>

