---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCredential.md
ms.openlocfilehash: 5f6ff2e89bd3b84a573e02a4584fe69794829453
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623624"
---
# <span data-ttu-id="342ba-101">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="342ba-101">Get-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="342ba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="342ba-102">SYNOPSIS</span></span>
<span data-ttu-id="342ba-103">取得自動化認證。</span><span class="sxs-lookup"><span data-stu-id="342ba-103">Gets Automation credentials.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="342ba-104">句法</span><span class="sxs-lookup"><span data-stu-id="342ba-104">SYNTAX</span></span>

### <span data-ttu-id="342ba-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="342ba-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="342ba-106">ByName</span><span class="sxs-lookup"><span data-stu-id="342ba-106">ByName</span></span>
```
Get-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="342ba-107">說明</span><span class="sxs-lookup"><span data-stu-id="342ba-107">DESCRIPTION</span></span>
<span data-ttu-id="342ba-108">**AzureRmAutomationCredential** Cmdlet 會取得一或多個 Azure 自動化認證。</span><span class="sxs-lookup"><span data-stu-id="342ba-108">The **Get-AzureRmAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="342ba-109">根據預設，會傳回所有認證。</span><span class="sxs-lookup"><span data-stu-id="342ba-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="342ba-110">指定認證的名稱以取得特定認證。</span><span class="sxs-lookup"><span data-stu-id="342ba-110">Specify the name of a credential to get a specific credential.</span></span>

<span data-ttu-id="342ba-111">為安全起見，這個 Cmdlet 不會傳回認證密碼。</span><span class="sxs-lookup"><span data-stu-id="342ba-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="342ba-112">示例</span><span class="sxs-lookup"><span data-stu-id="342ba-112">EXAMPLES</span></span>

### <span data-ttu-id="342ba-113">範例1：取得所有認證</span><span class="sxs-lookup"><span data-stu-id="342ba-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzureRmAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="342ba-114">這個命令會針對自動化帳戶（名為 Contoso17）中的所有認證取得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="342ba-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="342ba-115">範例2：取得認證</span><span class="sxs-lookup"><span data-stu-id="342ba-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzureRmAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="342ba-116">這個命令會在名為 Contoso17 的自動化帳戶中，為名為 ContosoCredential 的認證取得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="342ba-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="342ba-117">參數</span><span class="sxs-lookup"><span data-stu-id="342ba-117">PARAMETERS</span></span>

### <span data-ttu-id="342ba-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="342ba-118">-AutomationAccountName</span></span>
<span data-ttu-id="342ba-119">指定此 Cmdlet 為其檢索認證的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="342ba-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="342ba-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="342ba-120">-DefaultProfile</span></span>
<span data-ttu-id="342ba-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="342ba-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="342ba-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="342ba-122">-Name</span></span>
<span data-ttu-id="342ba-123">指定要取得認證的名稱。</span><span class="sxs-lookup"><span data-stu-id="342ba-123">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="342ba-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="342ba-124">-ResourceGroupName</span></span>
<span data-ttu-id="342ba-125">指定此 Cmdlet 為其檢索認證的資源群組。</span><span class="sxs-lookup"><span data-stu-id="342ba-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="342ba-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="342ba-126">CommonParameters</span></span>
<span data-ttu-id="342ba-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="342ba-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="342ba-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="342ba-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="342ba-129">輸入</span><span class="sxs-lookup"><span data-stu-id="342ba-129">INPUTS</span></span>

### <span data-ttu-id="342ba-130">所有</span><span class="sxs-lookup"><span data-stu-id="342ba-130">None</span></span>
<span data-ttu-id="342ba-131">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="342ba-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="342ba-132">輸出</span><span class="sxs-lookup"><span data-stu-id="342ba-132">OUTPUTS</span></span>

### <span data-ttu-id="342ba-133">CredentialInfo 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="342ba-133">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="342ba-134">筆記</span><span class="sxs-lookup"><span data-stu-id="342ba-134">NOTES</span></span>

## <span data-ttu-id="342ba-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="342ba-135">RELATED LINKS</span></span>

[<span data-ttu-id="342ba-136">新-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="342ba-136">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="342ba-137">移除-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="342ba-137">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)

[<span data-ttu-id="342ba-138">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="342ba-138">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


