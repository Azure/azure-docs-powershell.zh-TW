---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCredential.md
ms.openlocfilehash: cc5b347df5f60027ef67ff2bf9d00ad62ca66d6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448482"
---
# <span data-ttu-id="2e3b9-101">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="2e3b9-101">New-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="2e3b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2e3b9-102">SYNOPSIS</span></span>
<span data-ttu-id="2e3b9-103">建立自動化認證。</span><span class="sxs-lookup"><span data-stu-id="2e3b9-103">Creates an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e3b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="2e3b9-104">SYNTAX</span></span>

```
New-AzureRmAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e3b9-105">說明</span><span class="sxs-lookup"><span data-stu-id="2e3b9-105">DESCRIPTION</span></span>
<span data-ttu-id="2e3b9-106">**新的-AzureRmAutomationCredential** Cmdlet 會在 Azure 自動化中建立一個作為 **PSCredential** 物件的認證。</span><span class="sxs-lookup"><span data-stu-id="2e3b9-106">The **New-AzureRmAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="2e3b9-107">示例</span><span class="sxs-lookup"><span data-stu-id="2e3b9-107">EXAMPLES</span></span>

### <span data-ttu-id="2e3b9-108">範例1：建立認證</span><span class="sxs-lookup"><span data-stu-id="2e3b9-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2e3b9-109">第一個命令會將使用者名稱指派給 $User 變數。</span><span class="sxs-lookup"><span data-stu-id="2e3b9-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="2e3b9-110">第二個命令會使用 ConvertTo-SecureString Cmdlet，將純文字密碼轉換為安全字串。</span><span class="sxs-lookup"><span data-stu-id="2e3b9-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="2e3b9-111">該命令會將該物件儲存在 $Password 變數中。</span><span class="sxs-lookup"><span data-stu-id="2e3b9-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="2e3b9-112">第三個命令會根據 $User 和 $Password 建立認證，然後將其儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="2e3b9-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="2e3b9-113">最後一個命令會建立一個名為 ContosoCredential 的自動化認證，該認證使用 $Credential。</span><span class="sxs-lookup"><span data-stu-id="2e3b9-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="2e3b9-114">參數</span><span class="sxs-lookup"><span data-stu-id="2e3b9-114">PARAMETERS</span></span>

### <span data-ttu-id="2e3b9-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2e3b9-115">-AutomationAccountName</span></span>
<span data-ttu-id="2e3b9-116">指定此 Cmdlet 儲存認證的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="2e3b9-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e3b9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e3b9-117">-DefaultProfile</span></span>
<span data-ttu-id="2e3b9-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2e3b9-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e3b9-119">-描述</span><span class="sxs-lookup"><span data-stu-id="2e3b9-119">-Description</span></span>
<span data-ttu-id="2e3b9-120">指定認證的描述。</span><span class="sxs-lookup"><span data-stu-id="2e3b9-120">Specifies a description for the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e3b9-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="2e3b9-121">-Name</span></span>
<span data-ttu-id="2e3b9-122">指定認證的名稱。</span><span class="sxs-lookup"><span data-stu-id="2e3b9-122">Specifies a name for the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e3b9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e3b9-123">-ResourceGroupName</span></span>
<span data-ttu-id="2e3b9-124">指定此 Cmdlet 建立認證之資源群組的描述。</span><span class="sxs-lookup"><span data-stu-id="2e3b9-124">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

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

### <span data-ttu-id="2e3b9-125">-值</span><span class="sxs-lookup"><span data-stu-id="2e3b9-125">-Value</span></span>
<span data-ttu-id="2e3b9-126">將認證指定為 **PSCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="2e3b9-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e3b9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e3b9-127">CommonParameters</span></span>
<span data-ttu-id="2e3b9-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2e3b9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e3b9-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2e3b9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e3b9-130">輸入</span><span class="sxs-lookup"><span data-stu-id="2e3b9-130">INPUTS</span></span>

### <span data-ttu-id="2e3b9-131">System.object</span><span class="sxs-lookup"><span data-stu-id="2e3b9-131">System.String</span></span>

### <span data-ttu-id="2e3b9-132">系統管理. PSCredential</span><span class="sxs-lookup"><span data-stu-id="2e3b9-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="2e3b9-133">輸出</span><span class="sxs-lookup"><span data-stu-id="2e3b9-133">OUTPUTS</span></span>

### <span data-ttu-id="2e3b9-134">CredentialInfo 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2e3b9-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="2e3b9-135">筆記</span><span class="sxs-lookup"><span data-stu-id="2e3b9-135">NOTES</span></span>

## <span data-ttu-id="2e3b9-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="2e3b9-136">RELATED LINKS</span></span>

[<span data-ttu-id="2e3b9-137">AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="2e3b9-137">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="2e3b9-138">移除-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="2e3b9-138">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)

[<span data-ttu-id="2e3b9-139">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="2e3b9-139">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


