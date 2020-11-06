---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmDeletedWebApp.md
ms.openlocfilehash: 75ad4e1fabb511ee4ca3cff024389a8e826aeadd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449671"
---
# <span data-ttu-id="6b18f-101">Get-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="6b18f-101">Get-AzureRmDeletedWebApp</span></span>

## <span data-ttu-id="6b18f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6b18f-102">SYNOPSIS</span></span>
<span data-ttu-id="6b18f-103">在訂閱中取得已刪除的 web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="6b18f-103">Gets deleted web apps in the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b18f-104">句法</span><span class="sxs-lookup"><span data-stu-id="6b18f-104">SYNTAX</span></span>

```
Get-AzureRmDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b18f-105">說明</span><span class="sxs-lookup"><span data-stu-id="6b18f-105">DESCRIPTION</span></span>
<span data-ttu-id="6b18f-106">**AzureRmDeletedWebApp** Cmdlet 會傳回訂閱中所有已刪除的 web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="6b18f-106">The **Get-AzureRmDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="6b18f-107">您可以選擇性地依據 [資源] 群組、[名稱] 和 [槽] 篩選刪除的應用程式。</span><span class="sxs-lookup"><span data-stu-id="6b18f-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="6b18f-108">您可以有多個已刪除的應用程式，其名稱和資源群組都相同。</span><span class="sxs-lookup"><span data-stu-id="6b18f-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="6b18f-109">檢查 DeletionTime，以辨別共用相同名稱的已刪除 app。</span><span class="sxs-lookup"><span data-stu-id="6b18f-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="6b18f-110">示例</span><span class="sxs-lookup"><span data-stu-id="6b18f-110">EXAMPLES</span></span>

### <span data-ttu-id="6b18f-111">範例1</span><span class="sxs-lookup"><span data-stu-id="6b18f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="6b18f-112">這個命令會取得名為 ContosoSite 的已刪除應用程式，其名稱為「資源群組預設-Web-WestUS」。</span><span class="sxs-lookup"><span data-stu-id="6b18f-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="6b18f-113">參數</span><span class="sxs-lookup"><span data-stu-id="6b18f-113">PARAMETERS</span></span>

### <span data-ttu-id="6b18f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b18f-114">-DefaultProfile</span></span>
<span data-ttu-id="6b18f-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6b18f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b18f-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="6b18f-116">-Name</span></span>
<span data-ttu-id="6b18f-117">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b18f-117">The name of the web app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b18f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b18f-118">-ResourceGroupName</span></span>
<span data-ttu-id="6b18f-119">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b18f-119">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b18f-120">-槽</span><span class="sxs-lookup"><span data-stu-id="6b18f-120">-Slot</span></span>
<span data-ttu-id="6b18f-121">Web 應用程式槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b18f-121">The name of the web app slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b18f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b18f-122">CommonParameters</span></span>
<span data-ttu-id="6b18f-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6b18f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6b18f-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6b18f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b18f-125">輸入</span><span class="sxs-lookup"><span data-stu-id="6b18f-125">INPUTS</span></span>

### <span data-ttu-id="6b18f-126">所有</span><span class="sxs-lookup"><span data-stu-id="6b18f-126">None</span></span>

## <span data-ttu-id="6b18f-127">輸出</span><span class="sxs-lookup"><span data-stu-id="6b18f-127">OUTPUTS</span></span>

### <span data-ttu-id="6b18f-128">WebApps WebApps. PSAzureDeletedWebApp （）</span><span class="sxs-lookup"><span data-stu-id="6b18f-128">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="6b18f-129">筆記</span><span class="sxs-lookup"><span data-stu-id="6b18f-129">NOTES</span></span>

## <span data-ttu-id="6b18f-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="6b18f-130">RELATED LINKS</span></span>

[<span data-ttu-id="6b18f-131">Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="6b18f-131">Restore-AzureRmDeletedWebApp</span></span>](./Restore-AzureRmDeletedWebApp.md)
