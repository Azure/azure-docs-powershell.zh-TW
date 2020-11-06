---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiworkspacecollectionaccesskeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
ms.openlocfilehash: 61d71bebfd395b6856c93e0bc3642125437b5fe7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448983"
---
# <span data-ttu-id="53a4b-101">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="53a4b-101">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>

## <span data-ttu-id="53a4b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="53a4b-102">SYNOPSIS</span></span>
<span data-ttu-id="53a4b-103">取得與 Power BI 工作區集合相關聯的目前便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="53a4b-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53a4b-104">句法</span><span class="sxs-lookup"><span data-stu-id="53a4b-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIWorkspaceCollectionAccessKeys [-ResourceGroupName] <String>
 [-WorkspaceCollectionName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53a4b-105">說明</span><span class="sxs-lookup"><span data-stu-id="53a4b-105">DESCRIPTION</span></span>
<span data-ttu-id="53a4b-106">**AzureRmPowerBIWorkspaceCollectionAccessKeys** Cmdlet 會取得與 Power BI 工作區集合相關聯的目前便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="53a4b-106">The **Get-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="53a4b-107">示例</span><span class="sxs-lookup"><span data-stu-id="53a4b-107">EXAMPLES</span></span>

### <span data-ttu-id="53a4b-108">範例1：取得便捷鍵</span><span class="sxs-lookup"><span data-stu-id="53a4b-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollectionAccessKeys -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="53a4b-109">這個命令會取得指定資源群組中名為 WCN11 的工作區集合的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="53a4b-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="53a4b-110">參數</span><span class="sxs-lookup"><span data-stu-id="53a4b-110">PARAMETERS</span></span>

### <span data-ttu-id="53a4b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53a4b-111">-DefaultProfile</span></span>
<span data-ttu-id="53a4b-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="53a4b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53a4b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53a4b-113">-ResourceGroupName</span></span>
<span data-ttu-id="53a4b-114">指定集合之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="53a4b-114">Specifies the name of the resource group of the collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53a4b-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="53a4b-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="53a4b-116">指定此 Cmdlet 在其上執行的 Power BI 工作區集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="53a4b-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53a4b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53a4b-117">CommonParameters</span></span>
<span data-ttu-id="53a4b-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="53a4b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53a4b-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="53a4b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53a4b-120">輸入</span><span class="sxs-lookup"><span data-stu-id="53a4b-120">INPUTS</span></span>

### <span data-ttu-id="53a4b-121">System.object</span><span class="sxs-lookup"><span data-stu-id="53a4b-121">System.String</span></span>

## <span data-ttu-id="53a4b-122">輸出</span><span class="sxs-lookup"><span data-stu-id="53a4b-122">OUTPUTS</span></span>

### <span data-ttu-id="53a4b-123">PSWorkspaceCollectionAccessKey （PowerBIEmbedded.）。</span><span class="sxs-lookup"><span data-stu-id="53a4b-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="53a4b-124">筆記</span><span class="sxs-lookup"><span data-stu-id="53a4b-124">NOTES</span></span>

## <span data-ttu-id="53a4b-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="53a4b-125">RELATED LINKS</span></span>

[<span data-ttu-id="53a4b-126">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="53a4b-126">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>](./Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md)

