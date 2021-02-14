---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-AzWebAppCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
ms.openlocfilehash: 7988975daa512b44c71b17929f47d3318bfe192c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130231"
---
# <span data-ttu-id="0a089-101">Remove-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="0a089-101">Remove-AzWebAppCertificate</span></span>

## <span data-ttu-id="0a089-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0a089-102">SYNOPSIS</span></span>
<span data-ttu-id="0a089-103">針對 Azure Web App 建立應用程式服務管理的憑證。</span><span class="sxs-lookup"><span data-stu-id="0a089-103">Creates an App service managed certificate for an Azure Web App.</span></span> 

## <span data-ttu-id="0a089-104">句法</span><span class="sxs-lookup"><span data-stu-id="0a089-104">SYNTAX</span></span>

```
Remove-AzWebAppCertificate [-ResourceGroupName] <String> [-ThumbPrint] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a089-105">說明</span><span class="sxs-lookup"><span data-stu-id="0a089-105">DESCRIPTION</span></span>
<span data-ttu-id="0a089-106">**AzWebAppCertificate** Cmdlet 會建立 Azure App 服務管理的憑證</span><span class="sxs-lookup"><span data-stu-id="0a089-106">The **Remove-AzWebAppCertificate** cmdlet creates an Azure App Service Managed Certificate</span></span>

## <span data-ttu-id="0a089-107">示例</span><span class="sxs-lookup"><span data-stu-id="0a089-107">EXAMPLES</span></span>

### <span data-ttu-id="0a089-108">範例1</span><span class="sxs-lookup"><span data-stu-id="0a089-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" 
```

<span data-ttu-id="0a089-109">這個命令會移除指定 web 應用程式的應用程式服務受管理的憑證。</span><span class="sxs-lookup"><span data-stu-id="0a089-109">This command removes App Service Managed certificate for the given web app.</span></span>

## <span data-ttu-id="0a089-110">參數</span><span class="sxs-lookup"><span data-stu-id="0a089-110">PARAMETERS</span></span>

### <span data-ttu-id="0a089-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a089-111">-DefaultProfile</span></span>
<span data-ttu-id="0a089-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a089-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a089-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a089-113">-ResourceGroupName</span></span>
<span data-ttu-id="0a089-114">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a089-114">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a089-115">-指紋</span><span class="sxs-lookup"><span data-stu-id="0a089-115">-ThumbPrint</span></span>
<span data-ttu-id="0a089-116">已存在於網頁空間中的憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="0a089-116">Thumbprint of the certificate that already exists in web space.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a089-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a089-117">CommonParameters</span></span>
<span data-ttu-id="0a089-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0a089-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a089-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0a089-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a089-120">輸入</span><span class="sxs-lookup"><span data-stu-id="0a089-120">INPUTS</span></span>

### <span data-ttu-id="0a089-121">所有</span><span class="sxs-lookup"><span data-stu-id="0a089-121">None</span></span>

## <span data-ttu-id="0a089-122">輸出</span><span class="sxs-lookup"><span data-stu-id="0a089-122">OUTPUTS</span></span>

### <span data-ttu-id="0a089-123">System.void</span><span class="sxs-lookup"><span data-stu-id="0a089-123">System.Void</span></span>

## <span data-ttu-id="0a089-124">筆記</span><span class="sxs-lookup"><span data-stu-id="0a089-124">NOTES</span></span>

## <span data-ttu-id="0a089-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a089-125">RELATED LINKS</span></span>
[<span data-ttu-id="0a089-126">新-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="0a089-126">New-AzWebAppCertificate</span></span>](./New-AzWebAppCertificate.md)
