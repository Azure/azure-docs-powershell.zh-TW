---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportbitlockerkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
ms.openlocfilehash: 5f7a1fe5e8b80f6847bc3b3ca063d7166bf3ea95
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284395"
---
# <span data-ttu-id="8a0a8-101">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="8a0a8-101">Get-AzImportExportBitLockerKey</span></span>

## <span data-ttu-id="8a0a8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8a0a8-102">SYNOPSIS</span></span>
<span data-ttu-id="8a0a8-103">傳回指定作業中所有磁片磁碟機的 BitLocker 金鑰。</span><span class="sxs-lookup"><span data-stu-id="8a0a8-103">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="8a0a8-104">句法</span><span class="sxs-lookup"><span data-stu-id="8a0a8-104">SYNTAX</span></span>

```
Get-AzImportExportBitLockerKey -JobName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8a0a8-105">說明</span><span class="sxs-lookup"><span data-stu-id="8a0a8-105">DESCRIPTION</span></span>
<span data-ttu-id="8a0a8-106">傳回指定作業中所有磁片磁碟機的 BitLocker 金鑰。</span><span class="sxs-lookup"><span data-stu-id="8a0a8-106">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="8a0a8-107">示例</span><span class="sxs-lookup"><span data-stu-id="8a0a8-107">EXAMPLES</span></span>

### <span data-ttu-id="8a0a8-108">範例1：列出指定 ImportExport 作業中的所有 BitLocker 金鑰</span><span class="sxs-lookup"><span data-stu-id="8a0a8-108">Example 1: List all BitLocker Keys in specified ImportExport job</span></span>
```powershell
PS C:\> Get-AzImportExportBitLockerKey -JobName test-job -ResourceGroupName ImportTestRG 
BitLockerKey                                            DriveId
------------                                            -------
238810-662376-448998-450120-652806-203390-606320-483076 9CA995BA
```

<span data-ttu-id="8a0a8-109">這個 Cmdlet 會列出指定 ImportExport 作業中的所有 BitLocker 金鑰。</span><span class="sxs-lookup"><span data-stu-id="8a0a8-109">This cmdlet lists all BitLocker Keys in specified ImportExport job.</span></span>

## <span data-ttu-id="8a0a8-110">參數</span><span class="sxs-lookup"><span data-stu-id="8a0a8-110">PARAMETERS</span></span>

### <span data-ttu-id="8a0a8-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="8a0a8-111">-AcceptLanguage</span></span>
<span data-ttu-id="8a0a8-112">指定回應的喜好語言。</span><span class="sxs-lookup"><span data-stu-id="8a0a8-112">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="8a0a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a0a8-113">-DefaultProfile</span></span>
<span data-ttu-id="8a0a8-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8a0a8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a0a8-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="8a0a8-115">-JobName</span></span>
<span data-ttu-id="8a0a8-116">匯入/匯出作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a0a8-116">The name of the import/export job.</span></span>

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

### <span data-ttu-id="8a0a8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a0a8-117">-ResourceGroupName</span></span>
<span data-ttu-id="8a0a8-118">資源群組名稱會唯一識別使用者訂閱中的資源群組。</span><span class="sxs-lookup"><span data-stu-id="8a0a8-118">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="8a0a8-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a0a8-119">-SubscriptionId</span></span>
<span data-ttu-id="8a0a8-120">Azure 使用者的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="8a0a8-120">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="8a0a8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a0a8-121">CommonParameters</span></span>
<span data-ttu-id="8a0a8-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8a0a8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a0a8-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8a0a8-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a0a8-124">輸入</span><span class="sxs-lookup"><span data-stu-id="8a0a8-124">INPUTS</span></span>

## <span data-ttu-id="8a0a8-125">輸出</span><span class="sxs-lookup"><span data-stu-id="8a0a8-125">OUTPUTS</span></span>

### <span data-ttu-id="8a0a8-126">IDriveBitLockerKey （ImportExport）。 Api20161101。</span><span class="sxs-lookup"><span data-stu-id="8a0a8-126">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveBitLockerKey</span></span>

## <span data-ttu-id="8a0a8-127">筆記</span><span class="sxs-lookup"><span data-stu-id="8a0a8-127">NOTES</span></span>

<span data-ttu-id="8a0a8-128">別名</span><span class="sxs-lookup"><span data-stu-id="8a0a8-128">ALIASES</span></span>

## <span data-ttu-id="8a0a8-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="8a0a8-129">RELATED LINKS</span></span>

