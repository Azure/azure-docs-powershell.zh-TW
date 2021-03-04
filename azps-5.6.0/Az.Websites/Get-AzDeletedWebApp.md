---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
ms.openlocfilehash: a67e48cdcad9d80d244e74ef8e20f81fcbd157cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909894"
---
# <span data-ttu-id="a2321-101">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="a2321-101">Get-AzDeletedWebApp</span></span>

## <span data-ttu-id="a2321-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a2321-102">SYNOPSIS</span></span>
<span data-ttu-id="a2321-103">在訂閱中收到已刪除的 Web App。</span><span class="sxs-lookup"><span data-stu-id="a2321-103">Gets deleted web apps in the subscription.</span></span>

## <span data-ttu-id="a2321-104">語法</span><span class="sxs-lookup"><span data-stu-id="a2321-104">SYNTAX</span></span>

```
Get-AzDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2321-105">描述</span><span class="sxs-lookup"><span data-stu-id="a2321-105">DESCRIPTION</span></span>
<span data-ttu-id="a2321-106">**Get-AzDeletedWebApp** Cmdlet 會返回訂閱中所有已刪除的 Web App。</span><span class="sxs-lookup"><span data-stu-id="a2321-106">The **Get-AzDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="a2321-107">刪除的應用程式可選擇性地根據資源群組、名稱和時段進行篩選。</span><span class="sxs-lookup"><span data-stu-id="a2321-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="a2321-108">可以有一個已刪除的應用程式名稱和資源群組相同。</span><span class="sxs-lookup"><span data-stu-id="a2321-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="a2321-109">檢查 DeleteTime 以區別共用相同名稱的已刪除 App。</span><span class="sxs-lookup"><span data-stu-id="a2321-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="a2321-110">例子</span><span class="sxs-lookup"><span data-stu-id="a2321-110">EXAMPLES</span></span>

### <span data-ttu-id="a2321-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="a2321-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="a2321-112">此命令會獲得屬於資源群組 Default-Web-WestUS 的名為 ContosoSite 的已刪除應用程式。</span><span class="sxs-lookup"><span data-stu-id="a2321-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="a2321-113">參數</span><span class="sxs-lookup"><span data-stu-id="a2321-113">PARAMETERS</span></span>

### <span data-ttu-id="a2321-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2321-114">-DefaultProfile</span></span>
<span data-ttu-id="a2321-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2321-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2321-116">-位置</span><span class="sxs-lookup"><span data-stu-id="a2321-116">-Location</span></span>
<span data-ttu-id="a2321-117">已刪除 App 的位置。</span><span class="sxs-lookup"><span data-stu-id="a2321-117">The location of the deleted app.</span></span>

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

### <span data-ttu-id="a2321-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="a2321-118">-Name</span></span>
<span data-ttu-id="a2321-119">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2321-119">The name of the web app.</span></span>

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

### <span data-ttu-id="a2321-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2321-120">-ResourceGroupName</span></span>
<span data-ttu-id="a2321-121">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2321-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="a2321-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="a2321-122">-Slot</span></span>
<span data-ttu-id="a2321-123">Web App 插槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2321-123">The name of the web app slot.</span></span>

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

### <span data-ttu-id="a2321-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2321-124">CommonParameters</span></span>
<span data-ttu-id="a2321-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a2321-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2321-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a2321-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2321-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a2321-127">INPUTS</span></span>

### <span data-ttu-id="a2321-128">沒有</span><span class="sxs-lookup"><span data-stu-id="a2321-128">None</span></span>

## <span data-ttu-id="a2321-129">輸出</span><span class="sxs-lookup"><span data-stu-id="a2321-129">OUTPUTS</span></span>

### <span data-ttu-id="a2321-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="a2321-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="a2321-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a2321-131">NOTES</span></span>

## <span data-ttu-id="a2321-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2321-132">RELATED LINKS</span></span>

[<span data-ttu-id="a2321-133">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="a2321-133">Restore-AzDeletedWebApp</span></span>](./Restore-AzDeletedWebApp.md)