---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-AzWebAppCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
ms.openlocfilehash: adea8ace20b5e7c3c3c8d28161de53afdb431e19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909353"
---
# <span data-ttu-id="754fe-101">Remove-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="754fe-101">Remove-AzWebAppCertificate</span></span>

## <span data-ttu-id="754fe-102">簡介</span><span class="sxs-lookup"><span data-stu-id="754fe-102">SYNOPSIS</span></span>
<span data-ttu-id="754fe-103">移除 Azure Web App 的 App 服務受管理憑證。</span><span class="sxs-lookup"><span data-stu-id="754fe-103">Removes an App service managed certificate for an Azure Web App.</span></span> 

## <span data-ttu-id="754fe-104">語法</span><span class="sxs-lookup"><span data-stu-id="754fe-104">SYNTAX</span></span>

```
Remove-AzWebAppCertificate [-ResourceGroupName] <String> [-ThumbPrint] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="754fe-105">描述</span><span class="sxs-lookup"><span data-stu-id="754fe-105">DESCRIPTION</span></span>
<span data-ttu-id="754fe-106">**Remove-AzWebAppCertificate** Cmdlet 會移除 Azure 應用程式服務受管理的憑證</span><span class="sxs-lookup"><span data-stu-id="754fe-106">The **Remove-AzWebAppCertificate** cmdlet Removes an Azure App Service Managed Certificate</span></span>

## <span data-ttu-id="754fe-107">例子</span><span class="sxs-lookup"><span data-stu-id="754fe-107">EXAMPLES</span></span>

### <span data-ttu-id="754fe-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="754fe-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" 
```

<span data-ttu-id="754fe-109">此命令會移除給定 Web App 的應用程式服務受管理憑證。</span><span class="sxs-lookup"><span data-stu-id="754fe-109">This command removes App Service Managed certificate for the given web app.</span></span>

## <span data-ttu-id="754fe-110">參數</span><span class="sxs-lookup"><span data-stu-id="754fe-110">PARAMETERS</span></span>

### <span data-ttu-id="754fe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="754fe-111">-DefaultProfile</span></span>
<span data-ttu-id="754fe-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="754fe-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="754fe-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="754fe-113">-ResourceGroupName</span></span>
<span data-ttu-id="754fe-114">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="754fe-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="754fe-115">-ThumbPrint</span><span class="sxs-lookup"><span data-stu-id="754fe-115">-ThumbPrint</span></span>
<span data-ttu-id="754fe-116">Web 空間中已存在之憑證的指紋。</span><span class="sxs-lookup"><span data-stu-id="754fe-116">Thumbprint of the certificate that already exists in web space.</span></span>

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

### <span data-ttu-id="754fe-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="754fe-117">CommonParameters</span></span>
<span data-ttu-id="754fe-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="754fe-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="754fe-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="754fe-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="754fe-120">輸入</span><span class="sxs-lookup"><span data-stu-id="754fe-120">INPUTS</span></span>

### <span data-ttu-id="754fe-121">沒有</span><span class="sxs-lookup"><span data-stu-id="754fe-121">None</span></span>

## <span data-ttu-id="754fe-122">輸出</span><span class="sxs-lookup"><span data-stu-id="754fe-122">OUTPUTS</span></span>

### <span data-ttu-id="754fe-123">System.Void</span><span class="sxs-lookup"><span data-stu-id="754fe-123">System.Void</span></span>

## <span data-ttu-id="754fe-124">筆記</span><span class="sxs-lookup"><span data-stu-id="754fe-124">NOTES</span></span>

## <span data-ttu-id="754fe-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="754fe-125">RELATED LINKS</span></span>
[<span data-ttu-id="754fe-126">New-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="754fe-126">New-AzWebAppCertificate</span></span>](./New-AzWebAppCertificate.md)
