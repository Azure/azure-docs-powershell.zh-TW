---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/get-azimportexportbitlockerkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
ms.openlocfilehash: fefd529b00b88c20b3703e1bcecbbb88c72d52e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904673"
---
# <span data-ttu-id="467be-101">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="467be-101">Get-AzImportExportBitLockerKey</span></span>

## <span data-ttu-id="467be-102">簡介</span><span class="sxs-lookup"><span data-stu-id="467be-102">SYNOPSIS</span></span>
<span data-ttu-id="467be-103">針對指定工作的所有磁片磁碟機，會返回 BitLocker 鍵。</span><span class="sxs-lookup"><span data-stu-id="467be-103">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="467be-104">語法</span><span class="sxs-lookup"><span data-stu-id="467be-104">SYNTAX</span></span>

```
Get-AzImportExportBitLockerKey -JobName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="467be-105">描述</span><span class="sxs-lookup"><span data-stu-id="467be-105">DESCRIPTION</span></span>
<span data-ttu-id="467be-106">針對指定工作的所有磁片磁碟機，會返回 BitLocker 鍵。</span><span class="sxs-lookup"><span data-stu-id="467be-106">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="467be-107">例子</span><span class="sxs-lookup"><span data-stu-id="467be-107">EXAMPLES</span></span>

### <span data-ttu-id="467be-108">範例 1：列出指定 ImportExport 工作的所有 BitLocker 金鑰</span><span class="sxs-lookup"><span data-stu-id="467be-108">Example 1: List all BitLocker Keys in specified ImportExport job</span></span>
```powershell
PS C:\> Get-AzImportExportBitLockerKey -JobName test-job -ResourceGroupName ImportTestRG 
BitLockerKey                                            DriveId
------------                                            -------
238810-662376-448998-450120-652806-203390-606320-483076 9CA995BA
```

<span data-ttu-id="467be-109">此 Cmdlet 會列出指定 ImportExport 工作的所有 BitLocker 金鑰。</span><span class="sxs-lookup"><span data-stu-id="467be-109">This cmdlet lists all BitLocker Keys in specified ImportExport job.</span></span>

## <span data-ttu-id="467be-110">參數</span><span class="sxs-lookup"><span data-stu-id="467be-110">PARAMETERS</span></span>

### <span data-ttu-id="467be-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="467be-111">-AcceptLanguage</span></span>
<span data-ttu-id="467be-112">指定回應的偏好語言。</span><span class="sxs-lookup"><span data-stu-id="467be-112">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="467be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="467be-113">-DefaultProfile</span></span>
<span data-ttu-id="467be-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="467be-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="467be-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="467be-115">-JobName</span></span>
<span data-ttu-id="467be-116">匯進/匯出工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="467be-116">The name of the import/export job.</span></span>

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

### <span data-ttu-id="467be-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="467be-117">-ResourceGroupName</span></span>
<span data-ttu-id="467be-118">資源組名可唯一識別使用者訂閱中的資源群組。</span><span class="sxs-lookup"><span data-stu-id="467be-118">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="467be-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="467be-119">-SubscriptionId</span></span>
<span data-ttu-id="467be-120">Azure 使用者的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="467be-120">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="467be-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="467be-121">CommonParameters</span></span>
<span data-ttu-id="467be-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="467be-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="467be-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="467be-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="467be-124">輸入</span><span class="sxs-lookup"><span data-stu-id="467be-124">INPUTS</span></span>

## <span data-ttu-id="467be-125">輸出</span><span class="sxs-lookup"><span data-stu-id="467be-125">OUTPUTS</span></span>

### <span data-ttu-id="467be-126">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.models.Api20161101.IDriveBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="467be-126">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveBitLockerKey</span></span>

## <span data-ttu-id="467be-127">筆記</span><span class="sxs-lookup"><span data-stu-id="467be-127">NOTES</span></span>

<span data-ttu-id="467be-128">別名</span><span class="sxs-lookup"><span data-stu-id="467be-128">ALIASES</span></span>

## <span data-ttu-id="467be-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="467be-129">RELATED LINKS</span></span>

