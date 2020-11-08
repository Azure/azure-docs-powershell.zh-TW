---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
ms.openlocfilehash: 74c518d4713c19c7a1bb7b7d0b3341e164e22c35
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129073"
---
# <span data-ttu-id="68b0c-101">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="68b0c-101">Get-AzDeletedWebApp</span></span>

## <span data-ttu-id="68b0c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="68b0c-102">SYNOPSIS</span></span>
<span data-ttu-id="68b0c-103">在訂閱中取得已刪除的 web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="68b0c-103">Gets deleted web apps in the subscription.</span></span>

## <span data-ttu-id="68b0c-104">句法</span><span class="sxs-lookup"><span data-stu-id="68b0c-104">SYNTAX</span></span>

```
Get-AzDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68b0c-105">說明</span><span class="sxs-lookup"><span data-stu-id="68b0c-105">DESCRIPTION</span></span>
<span data-ttu-id="68b0c-106">**AzDeletedWebApp** Cmdlet 會傳回訂閱中所有已刪除的 web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="68b0c-106">The **Get-AzDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="68b0c-107">您可以選擇性地依據 [資源] 群組、[名稱] 和 [槽] 篩選刪除的應用程式。</span><span class="sxs-lookup"><span data-stu-id="68b0c-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="68b0c-108">您可以有多個已刪除的應用程式，其名稱和資源群組都相同。</span><span class="sxs-lookup"><span data-stu-id="68b0c-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="68b0c-109">檢查 DeletionTime，以辨別共用相同名稱的已刪除 app。</span><span class="sxs-lookup"><span data-stu-id="68b0c-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="68b0c-110">示例</span><span class="sxs-lookup"><span data-stu-id="68b0c-110">EXAMPLES</span></span>

### <span data-ttu-id="68b0c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="68b0c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="68b0c-112">這個命令會取得名為 ContosoSite 的已刪除應用程式，其名稱為「資源群組預設-Web-WestUS」。</span><span class="sxs-lookup"><span data-stu-id="68b0c-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="68b0c-113">參數</span><span class="sxs-lookup"><span data-stu-id="68b0c-113">PARAMETERS</span></span>

### <span data-ttu-id="68b0c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68b0c-114">-DefaultProfile</span></span>
<span data-ttu-id="68b0c-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="68b0c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68b0c-116">-位置</span><span class="sxs-lookup"><span data-stu-id="68b0c-116">-Location</span></span>
<span data-ttu-id="68b0c-117">已刪除的應用程式的位置。</span><span class="sxs-lookup"><span data-stu-id="68b0c-117">The location of the deleted app.</span></span>

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

### <span data-ttu-id="68b0c-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="68b0c-118">-Name</span></span>
<span data-ttu-id="68b0c-119">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="68b0c-119">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68b0c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68b0c-120">-ResourceGroupName</span></span>
<span data-ttu-id="68b0c-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="68b0c-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68b0c-122">-槽</span><span class="sxs-lookup"><span data-stu-id="68b0c-122">-Slot</span></span>
<span data-ttu-id="68b0c-123">Web 應用程式槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="68b0c-123">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68b0c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68b0c-124">CommonParameters</span></span>
<span data-ttu-id="68b0c-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="68b0c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68b0c-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="68b0c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68b0c-127">輸入</span><span class="sxs-lookup"><span data-stu-id="68b0c-127">INPUTS</span></span>

### <span data-ttu-id="68b0c-128">所有</span><span class="sxs-lookup"><span data-stu-id="68b0c-128">None</span></span>

## <span data-ttu-id="68b0c-129">輸出</span><span class="sxs-lookup"><span data-stu-id="68b0c-129">OUTPUTS</span></span>

### <span data-ttu-id="68b0c-130">WebApps WebApps. PSAzureDeletedWebApp （）</span><span class="sxs-lookup"><span data-stu-id="68b0c-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="68b0c-131">筆記</span><span class="sxs-lookup"><span data-stu-id="68b0c-131">NOTES</span></span>

## <span data-ttu-id="68b0c-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="68b0c-132">RELATED LINKS</span></span>

[<span data-ttu-id="68b0c-133">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="68b0c-133">Restore-AzDeletedWebApp</span></span>](./Restore-AzDeletedWebApp.md)